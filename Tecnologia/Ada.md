Tags: #tecnologia #programacao
Related: [[Tecnologia]], [[Linguagem de Programação]], [[C]]

17:05
## O que é?

É uma linguagem de programação estruturada, de tipagem estática, é uma linguagem imperativa, orientada a objetos e é uma linguagem de alto nível, originada de [[Pascal]], [[Simula]] e outras linguagens.
Foi criada por uma equipe liderada por Jean Ichbiah da CII Honeywell Bull, contratados pelo Departamento de Defesa dos Estados Unidos da América durante a década de 70, com o propósito de substituir todas as linguagens de programação utilizadas anteriormente por eles.
Recebeu este nome em homenagem à Ada Lovelace, considerada por muitos como sendo a primeira programadora da história.
É muito usada na área de desenvolvimento de [[Sistemas Críticos]], por ser uma linguagem forte e segura.

## Documentação

### Sumário

1. [[#Variáveis e constantes]]
2. [[#Tipos de Dados]]
3. [[#Comentários]] 

### Variáveis e constantes

Ada é uma linguagem *Case Insensitive*, o que significa que ao declarar um identificador, não importa se as letras estão maiúsculas ou minúsculas. Ex.: HELLO = Hello = HellO.

Quando uma variável é declarada, é preciso seguir algumas regras ao criar identificadores para variáveis ou ou funções, que são:
1. Iniciar com uma letra
2. Terminar com uma letra ou número
3. Não ter dois _ (*Underscores*) seguidos

Para definir uma variável, se escreve primeiro o nome/identificador dela, seguido por :, em seguido o tipo dela, o sinal de atribuição `:=` e, opcionalmente, o seu valor. Ex.:

```
A : Integer;          -- A = 0
B : Integer := 5;     -- B = 5
C : Integer := B;     -- C = 5   Pois no momento da declaração B = 5
D, E : Integer := 10; -- D = 10  E = 10
```

Caso queira declarar uma constante, é necessário adicionar o modificador `constant` antes de seu tipo. Ex.:
```
A : constant Integer := 5;
```

Não é permitido acessar variáveis antes delas serem declaradas. Ex.:

``` 
A : Integer := B; -- Erro de compilação   Pois 'B' ainda não foi declarado
B : Integer := 5; -- B = 5
```

Ada é uma linguagem fortemente tipada, o que significa que ao declarar um valor, ele será sempre do mesmo tipo até que ele seja explicitamente convertido. Ex.:

```
A : Integer := 10 * Integer (0.9); 
-- Converte o valor '0.9' de Float para Integer

A : Integer := Integer (Float (10) * 0.9); 
-- Converte '10' para Float, e em seguida converte o resultado da equação para   -- Integer
```

### Tipos de Dados

- Integer
- Float
- String
- Bollean
- List
- Tuple
- Dictionary
- Set
- Bytes e ByteArray
- None
- Classes
#### Tipos customizáveis

Para criar um tipo customizável em Ada, deve-se escrever a palavra `type`, seguido pelo nome do tipo e o seu *range*. Ex.:

```
type Score is range 0 .. 20;          -- Score = 1, 2, 3, ... 18, 19, 20
type Percentage is range -100 .. 100; -- Percentage = -100, -99, ... 99, 100

type Color is (Blue, Red, Green, Yellow, Purple);
type Ternary is (True, False, Unknown);
```

##### Criando tipos a partir de outros tipos customizáveis

É possível criar um tipo customizável em cima de outro tipo criado anteriormente. Para isso, a única coisa que você deve fazer de diferente é declarar um tipo novo e adicionar as palavras `is new`, seguidas do tipo em que está sendo baseado este. Ex.:

```
type Math_Score is new Score;
```

Você também pode restringir o *range* do novo tipo.

```
type Math_Score is new Score range 0 .. 10;
type Primary_Color is new Color range Red .. Blue;
```

#### Conversão de tipos

Em alguns casos, os tipos podem ser convertidos para outros. Mas somente se:
- Eles forem da mesma estrutura;
- Um é a derivação de outro;
Além disso, a conversão **deve** ser explícita.

```
V1 : Float := 0.0;
V2 : Integer := Integer (V1)
```

Antes de uma conversão, principalmente de tipos customizáveis, você deve fazer alguma verificação, caso contrário é possível que você receba um `Run-time error`. Ex.:

```
type T1 is range 0 .. 10;
type T2 is range 1 .. 10;

V1 : T1 := 0;
V2 : T2 := T2 (V1); -- Run-time error
```

Isso acontece pois o tipo `T1` possui em seu `range` o número zero e o tipo `T2` não. Então ao converter uma variável do tipo `T1` para o `T2` deve se fazer alguma verificação para ter certeza de que a variável a ser convertida está dentro do *range* do tipo a ser convertido, a fins de evitar erros.

### Operadores

#### Operadores Aritméticos

- `+` (soma)
- `-` (subtração)
- `*` (multiplicação)
- `/` (divisão)
- `**` (exponenciação)
- `rem` (resto de divisão)
- `mod` (resto de divisão sem sinal)
- `abs` (valor absoluto/sem o sinal)

#### Operadores de Comparação

- `=` (é igual à)
- `/=` (é diferente de)
- `<` (é menor que)
- `<=` (é menor ou igual à)
- `>` (é maior que)
- `>=` (é maior ou igual à)

#### Operadores Lógicos

- `and`
- `or`
- `xor` (`or` exclusivo)
- `not` (negação)

### Atributos

Em Ada, uma atributo pode ser acessado pelo sinal `'`. Ex.:

```
S : String := Integer'Image (42); -- Converte um Integer 42 para uma String "42"
```

### Comentários

Os comentários em Ada podem ser escritos da seguinte forma:

```
-- Comentário em Ada
```