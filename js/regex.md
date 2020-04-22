# Regex - Expressões Regulares :sparkles:
Uma expressão regular, ou Regex, são padrões utilizados para identificar determinadas combinações ou cadeias de caracteres em uma string. Ela faz parte do dia a dia de todos os programadores e administradores de infra. Por meio dela, podemos validar a entrada de usuários ou encontrar alguma informação em logs, documentação ou saída de comando. O mais legal é que as Regex são escritas independentes de uma linguagem, como JavaScript ou C#. As expressões são definidas em sua própria linguagem formal e uma vez aprendida, podemos aplicar o conhecimento dentro da linguagem de nossa preferência. Em outras palavras, linguagens como Java, JavaScript, C# e várias outras possuem uma implementação das expressões regulares e sabem interpretá-la.

## Onde são utilizadas?

**1. Na linha de comando**

Aplicar o Regex para encontrar um arquivo ou um conjunto de arquivos mais fácil. Podemos aplicar um filtro para encontrar. Nos editores também podemos usar na busca uma Regex.

**2. XSD, descrevem formato/padrão de um XML**

Você pode definir restrições, padrões para o XML.

## Apresentando o código
Qualquer Regex precisa ser interpretada por meio de uma Regex engine. Esse motor é uma parte de software que processa a expressão, tentando achar o padrão dentro da string dada, devolvendo os resultados. Normalmente a Regex engine faz parte da aplicação maior, para executar uma validação ou busca de uma string.

## Utilização no dia a dia
Uma tarefa muito comum no dia a dia do desenvolvedor é parsear um arquivo linha a linha, onde cada linha representa um dado ou registro. Há vários tipos de arquivos, e nesse curso vamos usar o exemplo de arquivo CSV, ou Comma-separated Values, por exemplo:

```
João Fulano,123.456.789-00,21 de Maio de 1993,(21) 3079-9987,Rua do Ouvidor,50,20040-030,Rio de Janeiro
Maria Fulana, 98765432100,11 de Abril de 1995,(11) 933339871,Rua Vergueiro,3185,04101-300,São Paulo
denise teste, 987.654.321.00,28 de Dezembro de 1991,(31)45562712,SCS Qd. 8 Bl. B-50,11,70333-900,Rio Grande
```

Então, em cada linha temos vários valores separados pela vírgula, por exemplo:

```
João Fulano,123.456.789-00,21 de Maio de 1093,(21) 3079-9987,Rua Buarque de Macedo,67,22220-232,Rio de Janeiro
```

Vamos supor que a gente queira extrair os número de CPF dessa linha através do *regex*. Qual o padrão de um CPF? Um CPF são 9 números, separados em blocos de 3 números por um ponto, mais um hífen e mais dois números. Para representar um número, podemos utilizar uma caracter class, que é um símbolo especial para representar um conjunto de caracteres. No mundo de *regex*, um número é representado pelo \d.

## O primeiro quantifier
Agora queremos que esse número apareça 3 vezes. O asterisco (*) significa 0, 1 ou mais vezes, ou seja, não atende. Queremos exatamente 3 números que podemos definir pela expressão \d{3}.

Dentro das chaves definimos a quantidade que o caractere deve estar presente. Com isso, já podemos encontrar 3 dígitos. Agora vem o "ponto" só que aprendemos que esse caractere possui um significado especial. No entanto queremos procurar o ponto literalmente e não qualquer caractere. Para deixar claro que o ponto deve ser ponto apenas, é preciso escapar o caractere com \. Assim temos:

```
\d{3}\.
```

Sabendo disso podemos definir o resto do CPF:

```
\d{3}\.\d{3}\.\d{3}\-\d{2}
```

## Um resumo
- Regex, ou expressões regulares, é uma linguagem para encontrar padrões de texto.
- Sendo uma linguagem independente, existem interpretadores para a maioria das plataformas de desenvolvimento, como JavaScript, C#, Python ou Ruby.
- Uma classe de caracteres predefinida é \d, que significa qualquer dígito.
- Existem vários meta-char, como . ou *.
- Existem quantifiers que definem quantas vezes um caractere deve aparecer:
{1} é um quantifier que significa uma vez.
- * é um quantifier que significa zero, uma ou mais vezes
- . é um meta-char que significa qualquer char.
- Com \ podemos escapar meta-chars, por exemplo \..