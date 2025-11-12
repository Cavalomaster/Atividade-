# 🧠 Conversor de Texto para Binário — Python

Este projeto é um programa simples em **Python** que solicita uma letra e uma lista de palavras, filtra as que começam com essa letra e converte cada uma delas para sua **representação binária** (8 bits por caractere).

---

## 📋 Funcionalidades
✅ Recebe uma letra digitada pelo usuário.  
✅ Recebe várias palavras separadas por espaço.  
✅ Filtra apenas as palavras que começam com a letra informada.  
✅ Converte cada palavra para código binário (usando o código Unicode de cada caractere).  
✅ Mostra o resultado no terminal.

---

## 🧩 Código completo

```python
def texto_para_binario(texto):
    return ' '.join(f"{ord(c):08b}" for c in texto)

def main():
    letra = input("Digite uma letra: ").strip().lower()
    palavras = input("Digite palavras separadas por espaço: ").split()

    print(f"\nPalavras que começam com '{letra}':\n")

    for palavra in palavras:
        if palavra.lower().startswith(letra):
            bin_palavra = texto_para_binario(palavra)
            print(f"Palavra: {palavra} | Binário: {bin_palavra}")

if __name__ == "__main__":
    main()
```

---

## 🪜 Passo a passo — Como executar o código

### 1. Instale o Python
Verifique se o Python está instalado:
```bash
python --version
```
Se não estiver, baixe em: [https://www.python.org/downloads/](https://www.python.org/downloads/)

### 2. Crie o arquivo do projeto
Crie um arquivo chamado **`conversor.py`** e cole o código acima nele.

### 3. Execute o script
Abra o terminal (ou prompt de comando) na pasta do arquivo e execute:
```bash
python conversor.py
```
ou, em alguns sistemas:
```bash
python3 conversor.py
```

---

## 🧠 Exemplo de uso

**Entrada:**
```
Digite uma letra: c
Digite palavras separadas por espaço: casa carro bola cachorro
```

**Saída:**
```
Palavras que começam com 'c':

Palavra: casa | Binário: 01100011 01100001 01110011 01100001
Palavra: carro | Binário: 01100011 01100001 01110010 01110010 01101111
Palavra: cachorro | Binário: 01100011 01100001 01100011 01101000 01101111 01110010 01110010 01101111
```

---

## 🧠 Explicação do código

- **`texto_para_binario()`** → Converte cada caractere do texto em binário com 8 bits.  
  - `ord(c)` retorna o valor numérico (Unicode) do caractere.  
  - `f"{ord(c):08b}"` formata o número como binário de 8 bits.  

- **`letra = input(...).strip().lower()`** → Lê a letra e padroniza para minúscula, removendo espaços.

- **`palavras = input(...).split()`** → Lê uma sequência de palavras e separa em uma lista.

- **`if palavra.lower().startswith(letra):`** → Verifica se a palavra começa com a letra informada.

- **`if __name__ == "__main__":`** → Garante que a função `main()` só execute se o script for rodado diretamente.

---

## 💡 Sugestões de melhoria
- Salvar a saída em um arquivo `.txt`.
- Criar uma versão com interface gráfica (Tkinter).
- Adicionar tratamento de erros para entrada vazia.
- Converter também frases completas, não apenas palavras.

---

## 🧑‍💻 Autor
**Seu Nome Aqui**  
📍 Projeto educacional em Python — Introdução à Lógica de Programação  
💾 Repositório: [https://github.com/SEU_USUARIO/conversor-binario](https://github.com/SEU_USUARIO/conversor-binario)
