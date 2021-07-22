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

## Visualizando um arquivo JAR
Para visualizar o conteúdo de um arquivo JAR pode ser utilizado o seguinte comando.
```
jar tf [arquivo-jar]
```
> O conteúdo será apresentado no _stdout_.
Em que:
- `t`: usado para ver a tabela de conteúdo do JAR.
- `f`: indica que o arquivo JAR que contém o conteúdo a ser mostrado será indicado por argumento.
- `arquivo-jar`: nome/caminho do arquivo JAR que contém o conteúdo a ser apresetado.

