# ⚡ Exercício jQuery - Formulários Interativos

![Status](https://img.shields.io/badge/Status-Concluído-green)
![jQuery](https://img.shields.io/badge/Library-jQuery-0769AD?logo=jquery&logoColor=white)
![HTML5](https://img.shields.io/badge/Code-HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/Style-CSS3-1572B6?logo=css3&logoColor=white)

> Uma aplicação focada na experiência do usuário (UX) em formulários, garantindo formatação visual e integridade de dados através da biblioteca jQuery.

## 🎯 Motivação e Propósito

A validação de dados e a facilidade de preenchimento são pilares fundamentais de qualquer aplicação web. O propósito deste projeto foi explorar o ecossistema do **jQuery** para resolver dois problemas comuns:
1.  **Entrada de Dados:** Ajudar o usuário a preencher campos formatados (CPF, Telefone, CEP) corretamente.
2.  **Validação (Client-Side):** Impedir o envio de formulários incompletos ou incorretos sem a necessidade de recarregar a página.

Este exercício demonstra o domínio sobre a manipulação eficiente do DOM e a integração de plugins externos para enriquecer a interface.

## 🛠️ Tecnologias Utilizadas

O projeto utiliza uma stack clássica e robusta para manipulação de interfaces:

* **[HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML):** Estrutura semântica do formulário.
* **[CSS3](https://developer.mozilla.org/pt-BR/docs/Web/CSS):** Estilização visual dos inputs, botões e feedbacks de erro.
* **[jQuery (Core)](https://jquery.com/):** Biblioteca principal para simplificar scripts e eventos do navegador.
* **[jQuery Mask Plugin](https://igorescobar.github.io/jQuery-Mask-Plugin/):** Plugin utilizado para criar máscaras de input (Ex: `000.000.000-00`).
* **[jQuery Validation](https://jqueryvalidation.org/):** Plugin para gerenciamento de regras de validação e mensagens de erro customizadas.

## 📦 Instalação e Execução

Este é um projeto estático (Client-Side), portanto, não requer instalação de servidores ou Node.js.

### Pré-requisitos
* Navegador Web atualizado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/DouglassenG/exercicio_jquery.git](https://github.com/DouglassenG/exercicio_jquery.git)
    ```

2.  **Acesse a pasta:**
    ```bash
    cd exercicio_jquery
    ```

3.  **Abra o projeto:**
    * Localize o arquivo `index.html`.
    * Abra-o diretamente no seu navegador (Chrome, Firefox, etc.).

## 💻 Uso e Funcionalidades

A aplicação consiste em um formulário de cadastro com os seguintes comportamentos programados:

* **Máscaras Automáticas:** Ao digitar no campo de telefone ou CPF, os caracteres de pontuação (pontos, traços, parênteses) são adicionados automaticamente.
* **Validação em Tempo Real:**
    * Campos obrigatórios exibem alertas visuais se deixados em branco.
    * O formato de e-mail é verificado antes do envio.

**Exemplo de Código (Lógica aplicada):**
```javascript
// Exemplo da inicialização das máscaras e validação no main.js
$(document).ready(function() {
    $('#telefone').mask('(00) 00000-0000');
    
    $('form').validate({
        rules: {
            nome: { required: true },
            email: { required: true, email: true }
        },
        messages: {
            nome: 'Por favor, insira seu nome completo.'
        }
    });
});
