Tags: #tecnologia #programacao 
Related: [[Tecnologia]], [[C++]], [[C-Sharp]] 

# O que é?



# Documentação



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
