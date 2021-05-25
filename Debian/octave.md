## Instalação de pacotes no octave

- Instalando pacotes através do Source Forge
```
pkg install [nome-pkg] -forge 
```
Use os parâmetros `-local` ou `-global` para definir o escopo de instalação apenas para o usuário ou para todo o sistema. 

- Instalando pacotes a partir de imagens baixadas. Faça download da imagem no [Source Forge](https://octave.sourceforge.io/packages.php) e após execute o seguinte comando:
```
pkg install [image-1.0.0.tar.gz]
```
- Para utilizar as funções dos pacotes após a instalação, é necessário carregar do pacote no octave com o seguinte comando:
```
pkg load image
```
- Para remover as funções do pacote que foram carregadas utilize a seguinte função:
```
pkg unload image
```
- Para desistalar um pacote use o comando abaixo
```
pkg uninstall [image]
```
- Use o seguinte comando para listar os pacotes instalados
```
pkg list
```
## Exemplo de configuração do octave

- Instalando o pacote `control`, `signal` e `communications` usando o Source Forge:
```
pkg install control -forge
pkg load control
pkg list

pkg install signal -forge
pkg load signal
pkg load communications

pkg list
```
