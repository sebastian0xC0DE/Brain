Tags: #programacao #tecnologia 
Related: [[C]], [[Software]]

# Sumário

1. [[#O que é?]]
2. [[#Documentação]]
	1. [[#Variáveis]]
	2. [[#Estruturas Condicionais]]
		1. [[#If Else]]
		2. [[#Loop For]]
	3. [[#Funções]]

# O que é?

Lua é uma linguagem de programação interpretada eficiente e leve. Ela permite programação em diversos estilos diferentes, como: Procedural, Orientada a Objetos, Funcional, Orientada a Dados, e Descrição de Dados.

Lua é tipada dinamicamente e é *Case Sensitive*, o que significa que você não precisa especificar o tipo das variáveis e a linguagem diferencia letras maiúculas de minúsculas.

# Documentação

## Variáveis

Para declarar uma variável em Lua, você deve escrever o nome da variável, seguido do sinal de igual ( = ) e o valor que você quer que ela receba.

```
numero = 10
palavra = "Lua"
boolean = True
table = {
	"primeiro", -- table[1]
	"segundo",  -- table[2]
	"terceiro", -- table[3]
}
```

## Estruturas Condicionais

Em lua existem várias estruturas condicionais, como *if else*, *loop while* e *loop for*.

### If Else

```
if x > 5 then
	print("maior")
else
	print("menor ou igual")
end
```

### Loop For

```
-- O loop continua até que a variável chegue a 10
for i = 1, 10 do
	print(i)
end
```

## Funções

```
function sum(a, b)
	return a + b
end
```
