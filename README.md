# 🧮 Calculadora Aritmética - Vue.js

![Status](https://img.shields.io/badge/Status-Finalizado-green)
![Vue.js](https://img.shields.io/badge/Framework-Vue.js-4FC08D?logo=vue.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-F7DF1E?logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/Style-CSS3-blue?logo=css3&logoColor=white)

> Uma Single Page Application (SPA) que demonstra o poder da reatividade do Vue.js aplicada à lógica matemática e interação em tempo real.

## 🎯 Motivação e Propósito

Calculadoras são o "Hello World" do gerenciamento de estado. O propósito deste projeto foi consolidar o entendimento sobre **Reatividade** e **Computed Properties**.

Diferente de calculadoras tradicionais que exigem um botão "Igual" (=) para processar, este projeto resolve a necessidade de feedback instantâneo. Ele demonstra como o Vue.js pode observar mudanças nos inputs (números e operadores) e recalcular o resultado automaticamente no DOM, sem recarregamentos ou ações explícitas de submissão.

## 🖼️ Demonstração Visual

*(Se o projeto estiver hospedado na Vercel, Netlify ou GitHub Pages, insira o link aqui. Ex: [Acesse a Calculadora Online](URL))*

## 🛠️ Tecnologias Utilizadas

A stack é focada na eficiência do framework progressivo:

* **[Vue.js](https://vuejs.org/):** Framework principal. Utilizado para:
    * **v-model:** Ligação bidirecional (Two-Way Binding) entre os campos de input e o estado da aplicação.
    * **Computed Properties:** Lógica de cálculo que se atualiza automaticamente apenas quando as dependências mudam, otimizando performance.
    * **Event Handling:** Captura da seleção de operações aritméticas.
* **[JavaScript (ES6+)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Lógica matemática e tratamento de dados.
* **[CSS3](https://developer.mozilla.org/pt-BR/docs/Web/CSS):** Estilização da interface.

## ✨ Funcionalidades

A aplicação oferece as operações fundamentais de forma dinâmica:

1.  **Entrada de Dados:** Dois campos de input numéricos para os operandos.
2.  **Seleção de Operação:** Dropdown (`<select>`) para escolher entre Soma (+), Subtração (-), Multiplicação (*) e Divisão (/).
3.  **Cálculo Reativo:** O resultado é exibido e atualizado instantaneamente conforme o usuário digita ou altera a operação.
4.  **Tratamento de Exceções:** Lógica para lidar com cenários como divisão por zero (se aplicável na implementação).

## 📂 Estrutura de Arquivos

O projeto segue a arquitetura padrão de componentes Vue, mantendo a organização limpa:

```text
calculadora_vue.js/
├── node_modules/        # Dependências do projeto
├── public/              # Assets estáticos (favicon, index.html base)
├── src/                 # Código Fonte
│   ├── components/      # Componentes Vue (ex: Calculadora.vue)
│   ├── App.vue          # Componente Raiz
│   └── main.js          # Inicialização da instância Vue
├── package.json         # Scripts e Dependências
└── README.md            # Documentação
