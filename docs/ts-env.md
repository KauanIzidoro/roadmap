# Requisitos - TypeScript

## 1. O que é TypeScript?
TypeScript é um superconjunto do JavaScript que adiciona tipagem estática ao código. Isso ajuda a evitar erros antes mesmo da execução e melhora a manutenção do código.

### Diferenciais do TypeScript:
- **Tipagem Estática**: Evita erros comuns de JavaScript ao definir tipos para variáveis e funções.
- **Suporte a ES6+**: Permite usar os recursos modernos do JavaScript.
- **Melhor Experiência de Desenvolvimento**: Ferramentas como IntelliSense melhoram a produtividade.
- **Facilidade de Refatoração**: A tipagem ajuda a encontrar erros ao modificar o código.

---

## 2. Instalando e Configurando TypeScript

### a) Instalando o Node.js
O TypeScript depende do Node.js para ser executado. Instale o [NodeJS](https://nodejs.org/pt)

Para verificar a instalação, abra o **Prompt de Comando (CMD)** e execute:
```sh
node -v
npm -v
```
Se aparecer um número de versão, significa que a instalação foi concluída com sucesso.

### b) Instalando o TypeScript
Abra o **CMD** e execute o seguinte comando para instalar o TypeScript globalmente:
```sh
npm install -g typescript
```
Para verificar se a instalação foi bem-sucedida, rode:
```sh
tsc -v
```
Se aparecer um número de versão, o TypeScript está instalado corretamente.

---

## 3. Criando um Projeto TypeScript

### a) Criando a pasta do projeto
No **CMD**, crie uma pasta para seu projeto e entre nela:
```sh
mkdir meu-projeto-ts
cd meu-projeto-ts
```

### b) Inicializando o TypeScript
Dentro da pasta do projeto, execute:
```sh
tsc --init
```
Isso cria um arquivo `tsconfig.json`, que define as configurações do compilador TypeScript.

### c) Criando um arquivo TypeScript
Abra o **Visual Studio Code (VSCode)**, abra a pasta do projeto e crie um arquivo `index.ts`. Adicione o seguinte código:
```ts
const mensagem: string = "Hello, TypeScript!";
console.log(mensagem);
```

### d) Compilando o código TypeScript
No terminal do **CMD** ou do **VSCode**, compile o arquivo TypeScript para JavaScript com:
```sh
tsc index.ts
```
Isso gera um arquivo `index.js`, que pode ser executado com:
```sh
node index.js
```
Se tudo estiver correto, a mensagem "Hello, TypeScript!" aparecerá no terminal.

---

## 4. Comandos Essenciais

### a) Compilar todos os arquivos TypeScript do projeto
No terminal do **CMD** ou **VSCode**, execute:
```sh
tsc
```
Isso compila todos os arquivos `.ts` com base no `tsconfig.json`.

### b) Compilar e monitorar mudanças automaticamente
Para evitar rodar o comando `tsc` manualmente toda vez, execute no terminal:
```sh
tsc --watch
```
Isso recompila automaticamente os arquivos TypeScript ao serem salvos.

### c) Rodar diretamente com ts-node (sem compilar para JS)
No terminal do **VSCode** ou **CMD**, instale o `ts-node`:
```sh
npm install -g ts-node
```
Agora você pode rodar arquivos `.ts` diretamente sem compilar:
```sh
ts-node index.ts
```

### d) Instalar dependências TypeScript
Se for usar bibliotecas que não possuem suporte nativo ao TypeScript, instale os tipos com:
```sh
npm install @types/express -D
```
Isso é útil para bibliotecas como Express, React, etc.

---

## 5. Conceitos Importantes do TypeScript

### a) Tipos Básicos
```ts
let nome: string = "João";
let idade: number = 25;
let ativo: boolean = true;
```

### b) Funções Tipadas
```ts
function soma(a: number, b: number): number {
  return a + b;
}
```

### c) Interfaces e Objetos
```ts
interface Usuario {
  nome: string;
  idade: number;
}

const usuario: Usuario = { nome: "Ana", idade: 30 };
```

### d) Classes e Herança
```ts
class Animal {
  nome: string;
  constructor(nome: string) {
    this.nome = nome;
  }
}

class Cachorro extends Animal {
  latir() {
    console.log("Au Au!");
  }
}
```

---

## 6. Como rodar TypeScript no Navegador
O TypeScript não é executado diretamente no navegador. Ele deve ser convertido para JavaScript antes. Para isso:

1. Compile o arquivo TypeScript:
   ```sh
   tsc index.ts
   ```
2. Crie um arquivo `index.html` e inclua o JavaScript gerado:
   ```html
   <!DOCTYPE html>
   <html lang="pt-BR">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>TypeScript no Navegador</title>
   </head>
   <body>
       <script src="index.js"></script>
   </body>
   </html>
   ```
3. Abra o `index.html` no navegador e veja o resultado no console (F12 > Console).

---
