# Processamento de Formulários e Arrays PHP

Este repositório contém um projeto simples desenvolvido em **HTML** e **PHP** focado no processamento de dados submetidos através de formulários e na manipulação de arrays. O nome do projeto, `2I-M5-12345-FP02`, sugere que se trata de um trabalho prático (FP02) do Módulo 5 (M5) de um curso técnico.

## Estrutura do Projeto

O projeto é composto por dois ficheiros principais:

| Ficheiro | Descrição |
| :--- | :--- |
| `form.html` | Contém o formulário de entrada de dados (frontend). |
| `lista.php` | Script PHP responsável por receber os dados submetidos e processá-los (backend). |

## Funcionalidades

O projeto demonstra duas funcionalidades distintas de processamento de dados, ambas acionadas a partir do `form.html` e processadas pelo `lista.php`.

### 1. Formulário de Entrada de Dados (`form.html`)

O ficheiro `form.html` apresenta dois formulários HTML distintos, ambos configurados para enviar dados para `lista.php` através do método `POST`.

*   **Primeiro Formulário (Itens):** Destinado à entrada de 5 itens genéricos (rotulados como "Item 1" a "Item 5").
*   **Segundo Formulário (Notas):** Destinado à entrada de 5 notas (rotuladas como "Nota 1" a "Nota 5").

**Nota Importante:** Foi identificada uma **inconsistência estrutural** no `form.html`. Os campos de input de ambos os formulários utilizam os mesmos atributos `name` (`item1` a `item5`). Na prática, apenas os valores do último formulário submetido serão processados corretamente pelo PHP, e o primeiro formulário não possui um botão de submissão (`<button type="submit">`).

### 2. Processamento de Dados (`lista.php`)

O script `lista.php` executa as seguintes tarefas:

#### A. Processamento da Lista de Compras/Notas

1.  Recebe os 5 valores submetidos via `POST` (variáveis `item1` a `item5`).
2.  Armazena estes valores num array PHP (`$itens`).
3.  Gera uma secção com o título **"Lista de Compras"**.
4.  Percorre o array `$itens` e exibe cada item numa lista não ordenada (`<ul>`), ignorando os campos que foram deixados vazios.

#### B. Demonstração de Arrays PHP

O script inclui uma secção adicional que demonstra a manipulação de arrays em PHP, com o título **"Tabela de Alunos e Idades"**.

*   Define um array associativo (`$turma`) e dois arrays indexados (`$alunos` e `$idades`).
*   O código tenta gerar uma tabela HTML (`<table border='1'>`) com base nestes arrays.

**Nota Importante:** A lógica de iteração e a construção da tabela HTML nesta secção estão **incorretas** e resultarão numa estrutura HTML inválida (list items `<li>` dentro de uma tabela `<table>` e iterações aninhadas que não produzem o resultado esperado de uma tabela de alunos e idades).

#### C. Secção "Classificação Automática"

Existe uma secção final com o título **"Classificação Automática"**, mas o código PHP para implementar esta funcionalidade está **ausente**.

## Tecnologias Utilizadas

*   **HTML5:** Estrutura dos formulários.
*   **PHP:** Lógica de backend para processamento de formulários e manipulação de arrays.

## Como Executar o Projeto

Para executar este projeto, é necessário um ambiente de servidor web que suporte PHP (e.g., Apache com módulo PHP).

1.  **Configuração do Servidor:** Instale um ambiente de desenvolvimento local como **XAMPP**, **MAMP**, ou **WAMP**.
2.  **Colocação dos Ficheiros:** Coloque os ficheiros `form.html` e `lista.php` no diretório raiz do seu servidor web (e.g., `htdocs` no XAMPP).
3.  **Acesso:** Abra o seu navegador e navegue para o endereço do ficheiro `form.html` (e.g., `http://localhost/form.html`).
4.  **Teste:** Preencha o segundo formulário (Notas) e clique em "Enviar" para ver o resultado no `lista.php`.
