


# TRABALHO: Valendo 50% da nota da 2ª prova.

__Abra este arquivo por meio do Preview do VSCode, ou leia-o diretamente pelo GitHub__

Faça um programa interativo que permita ao usuário do programa criar e manipular listas encadeadas. Cada item da lista deve ser uma string (array de char), representando uma lista de compras. Ou seja, o conteúdo de cada nó deve ser do tipo string.

O sistema deve apresentar um menu contendo as seguintes opções:

```
---------
#### Aplicação de lista de compras com listas encadeadas #####
Menu:
0. Imprimir lista
1. Criar nova lista vazia
2. Inserir elemento no início da lista
3. Inserir elemento no final da lista
4. Remover o elemento do início da lista
5. Remover o elemento do final da lista
6. Inserir um elemento no índice (posição)
7. Remover o elemento do índice (posição)
8. Inverter lista
9. Ler lista de arquivo
10. Gravar lista em arquivo
11. Sair

Digite a opção desejada: ****
```

O sistema deve imprimir esse menu na tela e aguardar que o usuário digite a opção desejada (números de 0 a 11, conforme os itens do menu).

Caso o usuário digite um número ou valor que não corresponda a uma das opções, o sistema deve imprimir um erro, mostrar novamente o menu e aguardar que o usuário digite novamente uma opção.


## Opção 11 - Sair

Se o usuário digitar a opção 9 (sair), o programa deve ser terminado (use o comando exit(EXIT_SUCCESS)).

## Opção 0 - Criar nova lista

Se o usuário digitar a opção 0 (zero), deve-se imprimir a lista da seguinte forma (supondo que haja 3 itens na lista):

	(1) arroz
	(2) feijão
	(3) macarrão

Caso a lista esteja vazia, deve-se imprimir: \<LISTA VAZIA\>. Uma vez que a lista é impressa, deve-se mostrar novamente o menu e aguardar a escolha da próxima ação do usuário.

## Opção 1 - Criar nova lista

Se o usuário digitar a opção 1 (um), deve-se criar uma nova lista vazia. Se uma lista já tinha sido criado antes, ela deve ser sobrescrita (ou seja, a lista anterior deixa de existir, "resetando-se" a lista).

### Cenário de Exemplo 1.1: 
Cria-se a lista vazia: \*cabeca -> NULL

## Opção 2 - Inserir elemento no início da lista

Se o usuário digitar a opção 2 (dois), deve-se imprimir "Digite o novo item a ser adicionado à lista: " (sem as aspas) e aguardar que o usuário digite o nome do item e aperte Enter. O item digitado deve então ser inserido na primeira posição da lista, antes de todos os demais elementos. Se a lista for vazia, insere-se no início.  

### Cenário de Exemplo 2.1: 
Lista vazia: \*cabeca -> NULL

- Usuário digita "feijao"

Lista após inserção: \*cabeca -> "feijao" -> NULL

### Cenário de Exemplo 2.2: 
Lista não vazia: \*cabeca -> "feijao"

- Usuário digita "arroz"

Lista após inserção: \*cabeca -> "arroz" -> "feijao" -> NULL

## Opção 3 - Inserir elemento no final da lista

Se o usuário digitar a opção 3 (três), deve-se imprimir "Digite o novo item a ser adicionado à lista: " (sem as aspas) e aguardar que o usuário digite o nome do item e aperte Enter. O item digitado deve então ser inserido no final da lista, após todos os demais elementos. Se a lista for vazia, insere-se no início. 

### Cenário de Exemplo 3.1: 
Lista vazia: \*cabeca -> NULL

- Usuário digita "feijao"

Lista após inserção: \*cabeca -> "feijao" -> NULL

### Cenário de Exemplo 3.2: 
Lista não vazia: \*cabeca -> "feijao"

- Usuário digita "arroz"

Lista após inserção: \*cabeca -> "feijao" -> "arroz" -> NULL

## Opção 4 - Remover o elemento do início da lista

Se o usuário digitar a opção 4 (quatro), deve-se remover o elemento do início da lista. Se a lista for vazia, deve-se imprimir uma mensagem de erro: "ERRO: Lista vazia"

### Cenário de Exemplo 4.1: 
Lista vazia: \*cabeca -> NULL

Imprime: "ERRO: Lista vazia"

### Cenário de Exemplo 4.2: 
Lista não vazia: \*cabeca -> "arroz" -> "feijao" -> NULL

Lista após remoção: \*cabeca -> \"feijao" -> NULL

## Opção 5 - Remover o elemento do final da lista

Se o usuário digitar a opção 5 (cinco), deve-se remover o elemento do final da lista. Se a lista for vazia, deve-se imprimir uma mensagem de erro: "ERRO: Lista vazia"

### Cenário de Exemplo 5.1: 
Lista vazia: \*cabeca -> NULL

Imprime: "ERRO: Lista vazia"

### Cenário de Exemplo 5.2: 
Lista não vazia: \*cabeca -> "arroz" -> "feijao" -> NULL

Lista após remoção: \*cabeca -> "arroz" -> NULL

## Opção 6 - Inserir em uma posição na lista

Se o usuário digitar a opção 6 (seis), deve-se inserir um elemento em uma posição na lista definida pelo usuário. Logo, o sistema deve imprimir "Digite o novo item a ser adicionado à lista: ", aguardar a resposta do usuário (similar ás opções 2 e 3), e em seguida imprimir "Digite a posição na lista em que se deseja inserir: ", e aguardar que o usuário digite o número correspondente à posição em que ele deseja que o item seja adicionado. Se o usuário digitar uma posição que seja maior que o tamanho atual da lista, deve-se imprimir um erro: "ERRO: posição inválida".

### Cenário de Exemplo 6.1: 
Lista não vazia: \*cabeca -> "arroz" -> "feijao" -> NULL

- Usuário digita o item "macarrao" e em seguida a posição 1 (segunda posição).

Lista após a inserção: \*cabeca -> "arroz" -> "macarrao" -> "feijao" -> NULL  (note que macarrão ficou na segunda posição, depois de "arroz" e antes de "feijao")

### Cenário de Exemplo 6.2: 
Lista não vazia: \*cabeca -> "arroz" -> "feijao" -> NULL

- Usuário digita o item "macarrao" e em seguida a posição 3 (quarta posição).

Imprime "ERRO: posição inválida", pois o tamanho da lista é 2, logo a posição digitada é maior que o tamanho da lista.

### Cenário de Exemplo 6.3: 
Lista vazia: \*cabeca -> NULL

- Usuário digita o item "arroz" e em seguida a posição 0 (primeira posição).

Lista após inserção: \*cabeca -> "arroz" -> NULL

### Cenário de Exemplo 6.4: 
Lista vazia: \*cabeca -> NULL
Usuário digita o item "arroz" e em seguida a posição 1 (segunda posição).

Imprime "ERRO: posição inválida", pois o tamanho da lista é 0, logo a posição digitada é maior que o tamanho da lista.

## Opção 7 - Remover de uma posição da lista

Se o usuário digitar a opção 7 (sete), deve-se remover o elemento da posição na lista. Logo, o sistema deve imprimir "Digite a posição na lista da qual se deseja remover: ", e aguardar que o usuário digite o número correspondente à posição em que ele deseja que o item seja removido. Se o usuário digitar uma posição que seja **maior ou igual** ao tamanho atual da lista, deve-se imprimir um erro: "ERRO: posição inválida". Se a lista for vazia, deve-se imprimir: "ERRO: Lista vazia"

### Cenário de Exemplo 7.1: 
lista não vazia: \*cabeca -> "arroz" -> "macarrao" -> "feijao" -> NULL

- Usuário digita a posição 1 (segunda posição).

lista após a remoção: \*cabeca -> "arroz" -> "feijao" -> NULL  (note que "macarrão" foi removido)

### Cenário de Exemplo 7.2: 
lista não vazia: \*cabeca -> "arroz" -> "macarrao" -> "feijao" -> NULL

- Usuário digita a posição 3 (quarta posição).

Imprime "ERRO: posição inválida", pois o tamanho da lista é 3, que é igual ao tamanho da lista.

### Cenário de Exemplo 7.3: 
lista vazia: \*cabeca -> NULL

Imprime "ERRO: Lista vazia"

## Opção 8 - Inverter lista

Se o usuário digitar a opção 8 (oito), deve-se inverter a lista.

### Cenário de Exemplo 8.1: 
lista não vazia: \*cabeca -> "arroz" -> "macarrao" -> "feijao" -> NULL

lista após inversão: \*cabeca -> "feijao" -> "macarrao" -> "arroz" -> NULL

### Cenário de Exemplo 8.2: 
lista vazia: \*cabeca -> NULL

lista após inversão: \*cabeca -> NULL


## Opção 9 - Carregar lista de arquivo

Se o usuário digitar a opção 9 (nove), deve-se solicitar que o usuário digite o caminho (_path_) do arquivo a ser carregado. O caminho é a sequência de diretórios (pastas) que se deve percorrer para acessar um arquivo. Por exemplo, supondo que seu arquivo se chame "lista_compras.txt" esteja na mesma pasta em que o programa é compilado e executado, então pode-se usar o caminho relativo, que no caso seria ou "lista_compras.txt" ou ".\lista_compras.txt" (Atenção: no Windows usa-se barra invertida ["\"] e no Linux usa-se barra normal ["/"]). Se o arquivo estiver em outra pasta, pode-se usar um caminho absoluto, como, por exemplo, "C:\User\Fulano\Documents".

Quanto ao formato do arquivo, deve simplesmente consistir nos nomes dos produtos da lista de compras separados por quebras de linha ("\n"). Por exemplo, um possível arquivo apareceria da seguinte forma quando aberto em um bloco de notas:

```
arroz
feijao
carne de boi
iogurte
```

Uma vez que o usuário tenha digitado o nome do arquivo a se ler, deve-se verificar se o arquivo existe. Se não existir, imprima uma mensagem de erro. Se existir, crie uma nova lista (ou seja, descarte-se a lista atual) e carregue os itens do arquivo na lista, mantendo-se a ordem em que eles aparecem no arquivo.

### Cenário de Exemplo 9.1: 

Seja um arquivo chamado "lista_compras1.txt" com o seguinte conteúdo:

```
arroz
feijao
carne de boi
```

Lista após carregamento: \*cabeca -> "arroz" -> "feijao" -> "carne de boi" -> NULL


## Opção 10 - Salvar lista em arquivo


Se o usuário digitar a opção 10 (dez), deve-se solicitar que o usuário digite o caminho (_path_) do arquivo a ser salvo, de modo similar ao que é feito na opção 9. Deve-se, então, salvar o conteúdo da lista atual no arquivo indicado. O formato do arquivo deve ser o mesmo do definido na opção 9. Caso o arquivo já possua dados, deve-se sobrescrever tudo pelo conteúdo da lista (ou seja, use opção "w" (write), sem "a" (append)).

### Cenário de Exemplo 10.1: 

Lista atual: \*cabeca -> "arroz" -> "feijao" -> "carne de frango" -> NULL

Usuário escolhe o nome do arquivo "lista_compras1_atualizado.txt".

Conteúdo do arquivo "lista_compras1_atualizado.txt" após gravação:

```
arroz
feijao
carne de frango
```