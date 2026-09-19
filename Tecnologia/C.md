Tags: #tecnologia #programacao 
Related: [[Tecnologia]], [[C++]], [[C-Sharp]] 

# Sumário

1. [[#O que é?]]
2. [[#Documentação]]
	1. [[#Variáveis]]
		1. [[#Tipos de Dados]]
			1. [[#Tipos Primitivos]]
			2. [[#Modificadores]]
	2. [[#Operações Bitwise]]
		1. [[#Como ligar um bit]]
		2. [[#Como desligar um bit]]
		3. [[#Como trocar o valor de um bit]]
		4. [[#Como verificar o valor de um bit]]

# O que é?



# Documentação

## Variáveis

### Tipos de Dados

#### Tipos Primitivos

| Nome   | Tipo                      | Tamanho   |
| ------ | ------------------------- | --------- |
| Bool   | Booleano                  | 1B ou 8b  |
| Char   | Caratere                  | 1B ou 8b  |
| Int    | Inteiro                   | 2B ou 16b |
| Float  | Real com precisão simples | 4B ou 32b |
| Double | Real com precisão dupla   | 8B ou 64b |
| Void   | Vazia / Sem valor         | 0b        |
#### Modificadores

| Nome     | Função                                             |
| -------- | -------------------------------------------------- |
| Signed   | Permite uma variável receber números com sinal     |
| Unsigned | Não permite uma variável receber números com sinal |
| Long     | Aumenta o tamanho de uma variável                  |
| Short    | Diminui o tamanho de uma variável                  |
## Operações Bitwise

### Como ligar um bit

```
// Passo a passo
char bit = 2;
char mascara;
mascara = 1 << bit;
arg = arg | mascara;

// Uma linha
arg |= (1 << bit)

// Com define
#define BitSet(arg, bit) ((arg) |= (1 << bit))
```

### Como desligar um bit

```
// Passo a passo
char bit = 2;
char mascara;
mascara = 1 << bit;
arg = arg & ~mascara;

// Uma linha
arg &= ~(1 << bit)

// Com define
#define BitSet(arg, bit) ((arg) &= ~(1 << bit))
```

### Como trocar o valor de um bit

```
// Passo a passo
char bit = 2;
char mascara;
mascara = 1 << bit;
arg = arg ^ mascara;

// Uma linha
arg ^= (1 << bit)

// Com define
#define BitSet(arg, bit) ((arg) ^= (1 << bit))
```

### Como verificar o valor de um bit

```
// Passo a passo
char bit = 2;
char mascara;
mascara = 1 << bit;
if (arg & mascara) {}

// Uma linha
if (arg & (1 << bit)) {}

// Com define
#define BitTst(arg, bit) ((arg) & (1 << bit))
```
