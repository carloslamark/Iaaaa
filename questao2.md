# Problema de Busca Heurística - Torre de Hanói
### O problema da Torre de Hanói é um clássico problema de quebra-cabeça que envolve mover discos de diferentes tamanhos de uma torre de origem para uma torre de destino, usando uma torre intermediária, respeitando a regra de que um disco maior nunca pode ser colocado em cima de um disco menor.

### Estado Inicial: Uma torre com N discos de tamanho diferente na primeira haste, com as hastes B e C vazias.

### Estado Objetivo: Todos os discos devem estar na terceira haste, ordenados pelo tamanho.


# Use a função de Heurística sendo a quantidade de peças fora do lugar:


```python

def heuristica_peças_fora_do_lugar(estado_atual, estado_objetivo):


    """
    Calcula o número de peças fora do lugar em relação ao estado objetivo.
    
    :estado_atual: O estado atual do quebra-cabeça.
    :estado_objetivo: O estado objetivo do quebra-cabeça.
    :returna: O número de peças fora do lugar.
    """


    n = len(estado_atual)
    count = 0
    
    for i in range(n):
        for j in range(n):
            if estado_atual[i][j] != estado_objetivo[i][j]:
                count += 1
    
    return count

```
