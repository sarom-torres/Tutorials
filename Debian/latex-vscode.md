## Configurações para o script [latexmk](https://mg.readthedocs.io/latexmk.html)
Author: Emerson Mello

Para quem usa a o script [latexmk](https://mg.readthedocs.io/latexmk.html) para compilar, abaixo são apresentadas [instruções](https://tex.stackexchange.com/questions/1226/how-to-make-latexmk-use-makeglossaries/1228#1228) que ajudam a gerar o glossário por meio dele. 

As instruções abaixo deve estar no arquivo `.latexmkrc`. O presente projeto já possui esse arquivo [.latexmkrc](.latexmkrc). Atente-se que é um arquivo oculto.

Todos os relatórios compartilham o mesmo arquivo de definição de classe LaTeX e imagem com o logo do IFSC. Sendo assim, esses arquivos foram colocados no diretório [arquivos-comuns](../arquivos-comuns) e a primeira linha do arquivo `.latexmkrc` redefine a variável de ambiente `TEXINPUTS` para o *script* latexmk possa encontrá-los. 

```perl
# Para deixar o cls e imagens PNG compartilhadas por todos os subdirestórios
$ENV{'TEXINPUTS'}='../../arquivos-comuns/:' . $ENV{'TEXINPUTS'}; 

# https://tex.stackexchange.com/questions/400325/latexmkrc-for-bib2gls
push @file_not_found, '^Package .* No file `([^\\\']*)\\\'';
print("GLOBAL LATEXMK: Glossaries Module...\n");

add_cus_dep('aux', 'glstex', 0, 'run_bib2gls');

sub run_bib2gls {
  if ( $silent ) {
    my $ret = system "bib2gls --silent --group '$_[0]'";
  } else {
    my $ret = system "bib2gls --group '$_[0]'";
  };
  my ($base, $path) = fileparse( $_[0] );
  if ($path && -e "$base.glstex") {
    rename "$base.glstex", "$path$base.glstex";
  }
  # Analyze log file.
  local *LOG;
  $LOG = "$_[0].glg";
  if (!$ret && -e $LOG) {
    open LOG, "<$LOG";
    while (<LOG>) {
      if (/^Reading (.*\.bib)\s$/) {
        rdb_ensure_file( $rule, $1 );
      }
    }
    close LOG;
  }
  return $ret;
}

$clean_ext .= ' %R.ist %R.xdy';
$clean_ext .= ' nav snm vrb run.xml';
```

### Versões atualizadas do latexmk e glossaries-extra

O ubuntu 18.04 LTS provê versões desatualizadas do latexmk e glossaries-extra. Para fazer uso das facilidades desse script e desse pacote, será necessário atualizar as versões. 

Primeiramente, é recomendado que instale os seguintes pacotes:

```bash
sudo apt-get install texlive-latex-base latexmk texlive-bibtex-extra texlive-lang-portuguese abntex texlive-latex-extra texlive-science texlive-fonts-extra biber texlive-publishers texlive-lang-english texlive-formats-extra texlive-font-utils openjdk-8-jdk
```

No diretório [aplicativos](../aplicativos) desse repositório encontrará versões necessárias para compilar esse modelo. Copie os arquivos para os seguintes caminhos (no Ubuntu 18.04):

```bash
sudo cp latexmk /usr/bin

sudo cp glossaries-extra-bib2gls.sty /usr/share/texlive/texmf-dist/tex/latex/glossaries-extra/
```

## Usando o [Visual Studio Code](https://code.visualstudio.com/) como IDE LaTeX

### Lista de extensões que deve instalar

- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- [bibtexLanguage](https://marketplace.visualstudio.com/items?itemName=phr0s.bib)
- [Brazilian Portuguese - Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-portuguese-brazilian)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

### Configurações do VSCode

Edite o arquivo `settings.json` (File -> Preferences -> Settings) e adicione dentro dele o bloco a seguir. Esse bloco contém instruções para o latexmk e faz com que os arquivos gerados com a compilação do projeto sejam colocados no subdiretório `outlatexdir`, inclusive o PDF.

> Use o VSCode para abrir o diretório desse projeto e não apenas para abrir o .tex. O VSCode trata diretório como workspace.

Com as configurações abaixo, sempre que salvar o arquivo .tex, o projeto será automaticamente compilado com o latexmk.

```json
"files.exclude": {
        "**/*.alg": true,
        "**/*.aux": true,
        "**/*.bbl": true,
        "**/*.bcf": true,
        "**/*.blg": true,
        "**/*.fdb_latexmk": true,
        "**/*.fls": true,
        "**/*.glg": true,
        "**/*.gls": true,
        "**/*.idx": true,
        "**/*.ind": true,
        "**/*.ist": true,
        "**/*.lof": true,
        "**/*.lol": true,
        "**/*.log": true,
        "**/*.lot": true,
        "**/*.nav": true,
        "**/*.out": true,
        "**/*.snm": true,
        "**/*.synctex*": true,
        "**/*.toc": true,
        "**/*.vrb": true,
        "**/*.xdy": true,
        "**/*.acr": true,
        "**/.classpath": true,
        "**/.factorypath": true,
        "**/.project": true,
        "**/.settings": true,
        "**/*.run.xml" : true,
        "**/*.acn": true,
        "**/*.glo": true
      },
      "latex-workshop.latex.clean.subfolder.enabled": true,
      "latex-workshop.synctex.afterBuild.enabled": true,
      "latex-workshop.latex.outDir": "%DIR%/outlatexdir",
      "latex-workshop.latex.recipe.default": "lastUsed",
      "latex-workshop.latex.recipes": [
      {
        "name": "latexmk",
        "tools": ["latexmk", "latexmk-clean"]
      }
      ],
      "latex-workshop.latex.tools": [
      {
        "name": "latexmk",
        "command": "latexmk",
        "args": [
          "-pdf",
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "-aux-directory=%OUTDIR%",
          "-outdir=%OUTDIR%",
          "%DOC%"
        ],
        "env": {}
      },
      {
        "name": "latexmk-clean",
        "command": "latexmk",
        "args": ["-bibtex", "-c", "-outdir=%OUTDIR%", "%DOC%"]
      },
      {
          "name": "pdflatex",
          "command": "pdflatex",
          "args": [
              "-synctex=1",
              "-interaction=nonstopmode",
              "-file-line-error",
              "-output-directory=%OUTDIR%",
              "%DOC%"
          ]
      },
       {
        "name": "xelatex",
        "command": "xelatex",
        "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "--aux-directory=%OUTDIR%",
          "--output-directory=%OUTDIR%",
          "%DOC%"
        ]
      },
      {
        "name": "biber",
        "command": "biber",
         "args": [
          "--input-directory=%OUTDIR%",
          "--output-directory=%OUTDIR%",
          "%DOCFILE%"
        ]
      },
      {
        "name": "makeglossaries",
        "command": "makeglossaries",
        "args": [
          "-d%OUTDIR%",
          "%DOCFILE%"
        ]
      }
    ],
    "latex-workshop.latex.clean.fileTypes": [
      "*.aux",
      "*.bbl",
      "*.blg",
      "*.bcf",
      "*.idx",
      "*.ind",
      "*.lof",
      "*.lol",
      "*.lot",
      "*.out",
      "*.toc",
      "*.acn",
      "*.acr",
      "*.alg",
      "*.glg",
      "*.glo",
      "*.gls",
      "*.fls",
      "*.log",
      "*.fdb_latexmk",
      "*.snm",
      "*.nav",
      "*.vrb",
      "*.run.xml",
      "*.xdy"
    ],
    "latex-workshop.message.update.show": false,
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.view.pdf.zoom": "page-width",
```
