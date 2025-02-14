teste
ta ai?
oi lindo
e ai cachorra
diogo gay





def adicionar_solucao(estoque, solucao, pH):
    """Adiciona uma solução química ao estoque, armazenando seu pH."""
    solucao_existe = False
    for item in estoque.keys():
        if item == solucao:  # Corrigido '=' para '=='
            solucao_existe = True
            break

    if solucao_existe is True:  # Mantida a estrutura original
        estoque[solucao] = pH  # Corrigido para atualizar o pH corretamente
    else:
        estoque[solucao] = pH


def remover_solucao(estoque, solucao):  # Corrigido nome do parâmetro
    """Remove uma solução química do estoque se ela existir."""
    
    contador = 0  # Corrigida a posição da inicialização da variável
    for item in estoque:
        if item == solucao:
            contador += 1
    
    if contador > 0:  # Ajustada a condição para remover corretamente
        estoque.pop(solucao)
    else:
        print(f"A solução {solucao} não está no estoque.")


def exibir_estoque(estoque):
    """Exibe as soluções químicas e seus respectivos níveis de pH."""
    for solucao in estoque:
        print(f"Solução {solucao}: pH {estoque[solucao]}")

# Estoque inicial como um dicionário vazio
estoque = {}


