# my_date_warlencintra
Meu dados
# 1. Store your data in a Python dictionary.
# This makes it organized and easy to read/update.
dados_pessoais = {
    "Nome Completo": "Warlen Xavier Cintra",
    "RG": "274828121",
    "CPF": "311.233.808-13", # Added standard formatting
    "Endereço": "Rua Aldeia Paracanti, 38, apto 1501, Vila Ré, São Paulo/SP",
    "CEP": "03667-020",
    "Celular": "+55 11 91736-0479", # Added standard formatting
    "E-mail": "warbear6@gmail.com",
    "Estado Civil": "Solteiro",
    "Profissão": "Professor e subempregado"
}

# 2. Define the name of the file you want to create
nome_do_arquivo = "dados_warlen.txt"

# 3. Use a 'with' block to safely open and write to the file.
# 'encoding="utf-8"' ensures special characters like 'ç' or 'ã' are saved correctly.
try:
    with open(nome_do_arquivo, 'w', encoding='utf-8') as arquivo:
        # Add a nice title to the file
        arquivo.write("INFORMAÇÕES PESSOAIS E PROFISSIONAIS\n")
        arquivo.write("="*40 + "\n\n") # This creates a separator line '======'

        # 4. Loop through each item in the dictionary
        for chave, valor in dados_pessoais.items():
            # Write each piece of data in the format "Label: Value"
            linha = f"{chave}: {valor}\n"
            arquivo.write(linha)
    
    # 5. Print a confirmation message to the user
    print(f"✅ Arquivo '{nome_do_arquivo}' foi criado com sucesso!")
    print("Você já pode abrir este arquivo no Microsoft Word.")

except Exception as e:
    print(f"❌ Ocorreu um erro ao criar o arquivo: {e}")
