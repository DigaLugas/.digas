# Interpretador Python (extensão .digas)

## Descrição

Este interpretador Python, com a extensão `.digas`, foi projetado para executar programas escritos em uma linguagem personalizada semelhante a assembly. O interpretador lê um arquivo de programa com a extensão `.digas`, analisa as instruções e as executa conforme necessário. A linguagem suporta operações aritméticas básicas, manipulação de pilha, operações de entrada/saída e instruções de fluxo de controle.

## Uso

**Instalação:** Não é necessária nenhuma instalação. Basta garantir que você tenha o Python instalado em seu sistema para executar o interpretador.

**Executando um Programa:**

Para executar um programa, use o seguinte comando no terminal:
```bash
python interpreter.py <arquivo_programa.digas>
```
Substitua `<arquivo_programa.digas>` pelo caminho do seu arquivo de programa.

## Sintaxe do Programa

- Cada linha no arquivo do programa representa uma instrução.
- As instruções são separadas por espaços.
- Instruções suportadas:
  - `push <valor>`: Adiciona um valor à pilha.
  - `pop`: Remove um valor da pilha.
  - `add`: Adiciona os dois valores do topo da pilha.
  - `sub`: Subtrai o valor do topo da pilha do segundo valor do topo.
  - `print <string>`: Imprime uma string literal.
  - `input`: Recebe a entrada do usuário e a adiciona à pilha.
  - `equal.0 <rótulo>`: Salta para o rótulo especificado se o valor do topo da pilha for igual a zero.
  - `greater.0 <rótulo>`: Salta para o rótulo especificado se o valor do topo da pilha for maior que zero.
  - `halt`: Encerra a execução do programa.
- Os rótulos terminam com dois pontos (:) e são usados para controle de fluxo.
- Comentários não são suportados nesta versão.

## Exemplo

Suponha que você tenha um arquivo de programa chamado `exemplo_programa.digas` com o seguinte conteúdo:
```python
read
equal.0 L1
LOOP:
push 2
sub
equal.0 L1
greater.0 LOOP
print "odd"
halt
L1:
print "even"
halt
halt
```
Executando este programa usando o interpretador:
```bash
python interpretador.py exemplo_programa.digas
```
Entrada: 3
```
Entrada: "odd"
```

## Licença

Este interpretador Python é fornecido sob a Licença MIT.

Sinta-se à vontade para modificar e expandir este README conforme necessário para o seu projeto de interpretador!
