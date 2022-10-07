# Curso de Java e java.io: Streams, Reader e Writers

**Faça esse curso de Java e:**

- Aprenda os fundamentos sobre java.io.

- Estabeleça entradas e saídas de fluxos diferentes.

- Saiba a diferença entre fluxos binários e fluxos de caracteres.

- Use a serialização Java e classe como Scanner, PrintStream ou Properties

- Entenda charsets e os problemas no encoding de caracteres

**Instrutor:** Nico Steppat

**Nesta aula aprendemos sobre alguns tópicos relacionados a leitura com Java IO:**

- Abertura de arquivos;

- Leitura linha a linha do arquivo e detecção de seu fim;

- Utilização de exceptions pelo Java IO caso a operação de leitura não saia como esperado;

- Classes abstratas e concretas para leitura.

Vamos continuar nossos estudos! Qualquer dúvida vá no fórum e pode nos falar!

### 01. Leitura com java.io

**Nesta aula aprendemos sobre alguns tópicos relacionados a leitura com Java IO:**

- Abertura de arquivos;

- Leitura linha a linha do arquivo e detecção de seu fim;

- Utilização de ***exceptions*** pelo Java IO caso a operação de leitura não saia como esperado;

- Classes abstratas e concretas para leitura.

Vamos continuar nossos estudos! Qualquer dúvida vá no fórum e pode nos falar!

### 02. Escrita com java.io

**Nesta aula aprendemos sobre alguns tópicos relacionados a escrita e flexibilidade do Java IO:**

- escrever em arquivos;

- escrever usando outputs diferentes;

- Ler e escrever dados abstraindo implementação;

- Classes abstratas e concretas para escrita e leitura.

Vamos continuar nossos estudos! Qualquer dúvida vá no fórum e pode nos falar!

### 03. FileWriter e PrintStream

**Nessa aula, vimos:**

- Várias alternativas para estabelecer uma saída para um arquivo de texto, como:

 - A classe FileWriter
 - A classe PrintStream
 - A classe PrintWriter

- Alguns detalhes da classe System, como :

 - O atributo System.out é do tipo PrintStream

 - O método System.lineSeparator() devolve os caracteres que representam uma nova linha
 
 - O método System.currentTimeMillis() devolve os milissegundos que passaram desde 1 de janeiro de 1970

 ### 04. Usando java.util.Scanner

**Nesta aula aprendemos mais sobre a Scanner e também formatacão de texto. Segue a lista:**

- Leitura de arquivos com Scanner

- Uso de delimitador com Scanner

- Formatação de texto e também de números

- Definição de Localização para formatar o texto.

### 05.  Encoding e Charsets

**Nessa aula você aprendeu sobre Unicode, Encodings e Charsets.**

Conheceu o problema dos **Encodings:** onde diferentes codepages são usados para escrever e exibir informações em seu computador. A solução foi dada por um consórcio que criou uma tabela genérica chamada **Unicode** contendo todos os caracteres do mundo em números denominados **codepoints**. A segunda parte da solução é aplicar diferentes Encodings para definir como os bytes são gravados nos arquivos. Os encodings são tabelas que transformam cada codepoint em seu caractere específico, dependendo de determinada região. Também observou que os encodings utilizados dependem muito de cada sistema operacional.

Usando o Windows, você implementou um programa para verificar a implementação do Java para Unicodes e Encodings e conheceu várias classes e métodos. Aprendeu que a classe String possui um método chamado **codePointAt()** para revelar o codepoint de determinado caractere a partir de sua posição na string. Descobriu que a classe que representa um encoding ou **Character Set** é **Charset** e o método estático para retornar uma referência com o charset default é **defaultCharset()**. Aprendeu que a classe String também possui um método para transformar os caracteres em bytes, o **getBytes()**, que usado sem argumento de entrada utiliza o charset padrão. Existem também duas sobrecargas para esse método, onde você pode informar o charset que deseja utilizar para a transformação. Conheceu a classe **StandardCharsets**, do pacote **java.nio**, que possui constantes pra os principais charsets. Por fim simulou o problema de encodings, gerando uma nova string a partir de um construtor que tinha como argumentos os bytes transformados no charset e o charset desejado para transformação. A solução foi garantir que o mesmo charset fosse aplicado, tanto na entrada quanto na saída.

As classes **Scanner** e **InputStreamReader** possuem sobrecargas de construtores que recebem como argumento qual charset será utilizado para fazer a transformação dos bytes em strings. De modo análogo para escrita, a classe **PrintWriter** também permite informar qual charset será utilizado para transformar a string nos bytes específicos.

### 06. Serialização de objetos

**Nesta aula, falamos bastante sobre a serialização de objetos com Java. Vimos que:**

- A criação do fluxo binário a partir de um objeto é chamado de **serialização**;

- A criação de um objeto a partir de um um fluxo binário é chamado de **desserialização**;

- A classe deve implementar a interface **java.io.Serializable**;

- A serialização/desserialização funciona em cascata e também com herança;

- Existe a palavra-chave **transient** para indicar que o atributo não deve ser serializado;

- É boa prática colocar o atributo estático **serialVersionUID** para versionar a classe;

- A versão sempre fica guardada no fluxo binário;

- Se não colocarmos explicitamente o **serialVersionUID**, a versão será gerada dinamicamente;

É raro usar a serialização na "unha", mas é um conhecimento importante, pois será utilizado por outras bibliotecas.