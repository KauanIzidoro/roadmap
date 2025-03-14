# Requisitos - Python

## 1. O que é Python?
Python é uma linguagem de programação de alto nível, interpretada e de tipagem dinâmica. É amplamente utilizada para desenvolvimento web, automação, análise de dados, machine learning e muito mais.

### Diferenciais do Python:
- **Sintaxe Simples**: Fácil de aprender e escrever.
- **Grande Ecossistema**: Milhares de bibliotecas e frameworks.
- **Multiparadigma**: Suporta programação procedural, orientada a objetos e funcional.
- **Alta Popularidade**: Comunidade ativa e muitos recursos de aprendizado.

---

## 2. Instalando e Configurando Python

### a) Instalando o Python
1. Acesse o site oficial do Python: [https://www.python.org/downloads/](https://www.python.org/downloads/).
2. Baixe a versão mais recente do Python para Windows.
3. Execute o instalador e marque a opção **"Add Python to PATH"**.
4. Clique em **"Install Now"** e aguarde a instalação ser concluída.

Para verificar a instalação, abra o **Prompt de Comando (CMD)** e execute:
```sh
python --version
```
Se aparecer um número de versão, significa que a instalação foi concluída com sucesso.

### b) Instalando o Gerenciador de Pacotes (pip)
O **pip** geralmente já vem instalado com o Python. Para verificar, execute:
```sh
pip --version
```
Caso precise instalar ou atualizar o pip, rode o seguinte comando:
```sh
python -m ensurepip --default-pip
python -m pip install --upgrade pip
```

---

## 3. Criando um Ambiente Virtual
Os ambientes virtuais permitem isolar dependências para diferentes projetos.

### a) Criando o ambiente virtual
Dentro da pasta do seu projeto, abra o **CMD** e execute:
```sh
python -m venv venv
```
Isso criará uma pasta chamada `venv` contendo o ambiente virtual.

### b) Ativando o ambiente virtual
Execute um dos seguintes comandos:
- No **CMD**:
  ```sh
  venv\Scripts\activate
  ```
- No **PowerShell**:
  ```sh
  venv\Scripts\Activate.ps1
  ```
- No **Git Bash**:
  ```sh
  source venv/Scripts/activate
  ```

O terminal exibirá `(venv)` antes do caminho, indicando que o ambiente está ativo.

### c) Instalando pacotes no ambiente virtual
Com o ambiente ativado, instale pacotes usando o `pip`:
```sh
pip install nome_do_pacote
```
Por exemplo:
```sh
pip install requests
```

Para salvar as dependências do projeto:
```sh
pip freeze > requirements.txt
```
Para reinstalar dependências em outro ambiente:
```sh
pip install -r requirements.txt
```

Para desativar o ambiente virtual, execute:
```sh
deactivate
```

---

## 4. Instalando e Configurando o Visual Studio Code
O **VS Code** é um editor leve e poderoso para programar em Python.

### a) Instalando o VS Code
1. Baixe e instale o **VS Code** em: [https://code.visualstudio.com/](https://code.visualstudio.com/).
2. Durante a instalação, marque a opção "Add to PATH".
3. Abra o **VS Code** e instale a extensão **Python** (Microsoft) na aba "Extensions" (`Ctrl+Shift+X`).

### b) Configurando o ambiente Python no VS Code
1. Abra seu projeto no VS Code (`File > Open Folder`).
2. Pressione `Ctrl+Shift+P` e procure por `Python: Select Interpreter`.
3. Selecione o caminho do Python dentro do ambiente virtual (`venv\Scripts\python.exe`).
4. No terminal do VS Code, ative o ambiente virtual e inicie seu projeto.

---

## 5. Executando Scripts Python

### a) Criando um arquivo Python
1. No **VS Code**, crie um arquivo `main.py` e adicione o seguinte código:
   ```python
   print("Hello, Python!")
   ```

2. Para executar, abra o terminal no **VS Code** e rode:
   ```sh
   python main.py
   ```

### b) Executando no terminal diretamente
No **CMD**, **PowerShell** ou **Git Bash**, navegue até a pasta do arquivo e execute:
```sh
python main.py
```

---

## 6. Comandos Essenciais

### a) Verificar versão do Python e pip
```sh
python --version
pip --version
```

### b) Criar e ativar ambiente virtual
```sh
python -m venv venv
venv\Scripts\activate
```

### c) Instalar pacotes
```sh
pip install nome_do_pacote
```

### d) Gerar arquivo de dependências
```sh
pip freeze > requirements.txt
```

### e) Instalar dependências de um projeto
```sh
pip install -r requirements.txt
```

### f) Desativar ambiente virtual
```sh
deactivate
```

---

## 7. Estrutura de um Projeto Python
Uma estrutura recomendada para projetos Python:
```
meu_projeto/
│-- venv/               # Ambiente virtual
│-- src/                # Código-fonte
│   ├── main.py         # Arquivo principal
│   ├── modulo.py       # Módulo adicional
│-- tests/              # Testes
│-- requirements.txt    # Dependências
│-- .gitignore          # Arquivos ignorados pelo Git
│-- README.md           # Documentação do projeto
```
---

Agora seu ambiente de desenvolvimento Python no Windows está configurado e pronto para uso!

