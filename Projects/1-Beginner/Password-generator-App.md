# 🔑[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Press+Start+2P&size=15&pause=1000&color=F7EE3D&width=435&lines=Gerador+de+senhas+aleat%C3%B3rias)](https://git.io/typing-svg)

**Tier:** 1-Beginner

Um gerador de senhas simples e personalizável feito em **Python**.  
Permite ao usuário definir o tamanho da senha e escolher quais tipos de caracteres incluir: letras maiúsculas, letras minúsculas, números e símbolos.  

**Propósito da aplicação:**  
O objetivo é fornecer uma forma rápida e prática de criar senhas seguras para contas, serviços e sistemas, evitando senhas fracas e fáceis de adivinhar.  

**Recursos necessários:**  
- Python 3 instalado  
- Nenhuma biblioteca externa (somente `random` e `string` da biblioteca padrão do Python)  

---

## User Stories

- [ ] User can define password length
- [ ] User can choose whether to include uppercase letters
- [ ] User can choose whether to include lowercase letters
- [ ] User can choose whether to include numbers
- [ ] User can choose whether to include special symbols
- [ ] User receives a warning if no character type is selected

---
    ```py
    import random
    import string

    def gerar_senha(tamanho=12,maiusculas=True, minusculas=True,numeros=True, simbolos=True):
        caracteres = ""
    
        if maiusculas:
            caracteres += string.ascii_uppercase   
    
        if minusculas:
            caracteres += string.ascii_lowercase
        
        if numeros:
            caracteres += string.digits
        
        if simbolos:
            caracteres += "!@#$^&*()_+-[]{}|;:.<>?"
        
        if not caracteres:
            return "Nenhum tipo de caractere selecionado!"
    
    senha = ''.join(random.choice(caracteres) for _ in range(tamanho))
    return senha

    print("===Gerador de Senha===")

    tamanho = int (input ("Digite tamanho da senha, quantos digitos?: "))
    usar_maiusculas = input("Incluir letras maiusculas? (s/n): ").lower()=="s"
    usar_minusculas = input("Incluir letras minusculas? (s/n): ").lower()=="s"
    usar_numeros = input("Incluir números? (s/n): ").lower()== "s"
    usar_simbolos = input("Incluir simbolos? (s/n): ").lower()=="s"

    senha = gerar_senha(tamanho, usar_maiusculas, usar_minusculas,usar_numeros,usar_simbolos)

    print(f"\n Sua senha gerada: {senha}")

## Bonus features

- [ ] User can view password strength (weak, medium, strong)
- [ ] User can copy the generated password to the clipboard
- [ ] User can generate multiple passwords in sequence
- [ ] Graphical interface for ease of use
- [ ] Option to save generated passwords to a local file  

---

##  Useful links and resources

- [Documentação oficial do Python](https://docs.python.org/3/)  
- [Documentação do módulo `random`](https://docs.python.org/3/library/random.html)  
- [Documentação do módulo `string`](https://docs.python.org/3/library/string.html)  
- [Artigo sobre criação de senhas seguras](https://www.kaspersky.com/resource-center/threats/how-to-create-a-strong-password)  

---

## Example projects

- [Gerador de Senhas Python no GeeksforGeeks](https://www.geeksforgeeks.org/password-generator-using-python/)  
- [Password Generator App – GitHub](https://github.com/topics/password-generator)
