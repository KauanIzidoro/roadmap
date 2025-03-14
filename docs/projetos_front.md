# 🎨*TypeScript* aplicado ao Frontend

## 💻 Criando um Projeto

### a) Frameworks Disponíveis
TypeScript pode ser usado com diversos frameworks e bibliotecas frontend, como:
- **React**: Popular para construção de interfaces modernas e reutilizáveis.
- **Vue.js**: Leve e fácil de aprender, ideal para aplicações menores.
- **Angular**: Completo e robusto, adequado para aplicações empresariais.
- **Svelte**: Alternativa minimalista e eficiente, focada em performance.

### b) Quando Usar Cada Framework?
- **React**: Quando precisa de uma comunidade grande, suporte a bibliotecas externas e flexibilidade.
- **Vue.js**: Se busca um aprendizado rápido e uma sintaxe amigável.
- **Angular**: Para projetos complexos que exigem estrutura sólida e escalabilidade.
- **Svelte**: Se deseja performance máxima com menos código.

### c) Criando um Projeto Simples com TypeScript no Frontend
Vamos criar um projeto simples usando **Vite + React + TypeScript**.

#### O que é Vite?
Vite é uma ferramenta de build rápida para projetos frontend. Ele otimiza o tempo de desenvolvimento ao fornecer um servidor de desenvolvimento rápido e um processo de build eficiente.

#### Passo a passo para criar o projeto:
1. **Crie o projeto** no terminal do **CMD** ou **VSCode**:
   ```sh
   npm create vite@latest meu-app --template react-ts
   ```
   - `npm create vite@latest`: Baixa e executa o gerador de projetos do Vite.
   - `meu-app`: Nome do diretório do projeto.
   - `--template react-ts`: Define o template como React com TypeScript.

2. **Entre na pasta do projeto**:
   ```sh
   cd meu-app
   ```
   - `cd meu-app`: Acessa a pasta recém-criada do projeto.

3. **Instale as dependências**:
   ```sh
   npm install
   ```
   - `npm install`: Baixa e instala todas as bibliotecas necessárias para rodar o projeto.

4. **Inicie o servidor local**:
   ```sh
   npm run dev
   ```
   - `npm run dev`: Inicia o servidor local de desenvolvimento.
   - O projeto será acessível em `http://localhost:5173`.

### d) Código Simples para Exibir uma Mensagem
Abra `src/App.tsx` e substitua o conteúdo por:
```tsx
import { useState } from "react";

function App() {
  const [mensagem, setMensagem] = useState("Olá, TypeScript!");
  
  return (
    <div>
      <h1>{mensagem}</h1>
      <button onClick={() => setMensagem("Você clicou!")}>Clique aqui</button>
    </div>
  );
}

export default App;
```

Salve e veja o resultado no navegador!

---

## 🚀 Desafio
Agora que você criou um projeto TypeScript para frontend, aqui está um desafio:

**Crie um contador simples**:
- Adicione dois botões: um para aumentar e outro para diminuir um número.
- Exiba o número na tela.
- Use **useState** para gerenciar o estado do contador.

Dica: Modifique o `App.tsx` para incluir um estado `count` e manipular sua atualização ao clicar nos botões.
