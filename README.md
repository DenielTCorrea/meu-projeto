Olá! Meu nome é Deniel Tillmann Correa e sou estudante de Análise e Desenvolvimento de Sistemas.

Tenho grande interesse em desenvolvimento de software e resolução de problemas através do código. Atualmente, estou focando no aprendizado construindo projetos práticos para consolidar conceitos de estrutura de dados, algoritmos e boas práticas de desenvolvimento.

💼 Objetivo: Buscando oportunidades para aplicar e expandir meus conhecimentos no mercado de tecnologia.
🌐 LinkedIn: Deniel Tillmann Correa
✉️ Contato: deniel.tillmannc@gmail.com

# Lista para armazenar os produtos do estoque
estoque = []

def exibir_menu():
    print("\n--- GERENCIADOR DE ESTOQUE ---")
    print("1. Cadastrar Produto")
    print("2. Listar Produtos")
    print("3. Sair")

while True:
    exibir_menu()
    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        nome = input("Nome do produto: ")
        quantidade = int(input("Quantidade: "))
        preco = float(input("Preço unitário: "))
        
        # Salvando em um dicionário
        produto = {"nome": nome, "quantidade": quantidade, "preco": preco}
        estoque.append(produto)
        print(f"Produto '{nome}' cadastrado com sucesso!")

    elif opcao == "2":
        print("\n--- LISTA DE PRODUTOS ---")
        if len(estoque) == 0:
            print("Estoque vazio.")
        else:
            for i, p in enumerate(estoque):
                print(f"{i+1}. Nome: {p['nome']} | Qtd: {p['quantidade']} | Preço: R$ {p['preco']:.2f}")

    elif opcao == "3":
        print("Saindo do sistema. Até mais!")
        break
    else:
        print("Opção inválida, tente novamente.")
