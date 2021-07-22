# Arquivo JAR

## Criando um arquivo JAR

O comando abaixo pode ser utilizado para criar um arquivo JAR.
```
jar cf [arquivo-jar].jar [arquivos-de-entrada]
```
Em que:
- `c`: usado para criar um arquivo JAR.
- `f`: direciona a saída para um arquivo ao invés do _stdout_.
- `arquivo-jar`: nome/caminho do arquivo JAR resultante ao final da operação. Por convenção, é utilizada a extensão `.jar`.
- `arquivos-de-entrada`: um ou mais arquivos a serem incluídos no arquivo JAR. É utilizado `*` inserir recursovamente arquivos que estão dentro de diretórios. 

## Visualizando conteúdo de um arquivo JAR
Para visualizar o conteúdo de um arquivo JAR pode ser utilizado o seguinte comando.
```
jar tf [arquivo-jar]
```
> O conteúdo será apresentado no _stdout_.
Em que:
- `t`: usado para ver a tabela de conteúdo do JAR.
- `f`: indica que o arquivo JAR que contém o conteúdo a ser mostrado será indicado por argumento.
- `arquivo-jar`: nome/caminho do arquivo JAR que contém o conteúdo a ser apresentado.

## Extraíndo conteúdo de um arquivo JAR
O comando abaixo pode ser usado para extrair o conteúdo de um arquivo JAR.
```
jar xf [arquivo-jar] [arquivos-extraidos]
```
Em que:
- `c`: usado indicar que será realizada a extração do conteúdo de um arquivo JAR.
- `f`: indica que o arquivo JAR que contém o conteúdo a ser extraído será informado por argumento.
- `arquivo-jar`: nome/caminho do arquivo JAR que contém o conteúdo a ser extraído.
- `arquivos-extraidos`: argumento opcional contendo uma lista de arquivos (separados apenas por espaços) a serem extraídos do JAR. Caso esse argumento não seja incluído serão extraídos todos os arquivos.

## Atualizando um arquivo JAR
Para atualizar ou inserir novos aqruivos em um arquivo JAR o seguinte comando pode ser utilizado:
```
jar uf [arquivo-jar] [arquivos-de-entrada]
```
Em que:
- `u`: usado para indicar que o arquivo JAR será atualizado.
- `f`: indica que o arquivo JAR a ser atualizado será informado por argumento.
- `arquivo-jar`: nome/caminho do arquivo JAR já existente e que deverá ser atualizado.
- `arquivos-de-entrada`: lista de um ou mais arquivos (separados por espaços) a serem atualizados ou adicionadoso arquivo do JAR. 
> Todos os arquivos existentes que possuam os mesmos nomes da lista informada serão sobrescritos.

## Executando um arquivo JAR
Utlize o seguinte comando para executar um arquivo JAR:
```
java -jar [arquivo-jar]
```
