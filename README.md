# VetCare - Hospital Veterinário e Centro Diagnóstico 🐾

![VetCare Banner](https://placehold.co/1200x400/059669/ffffff?text=VetCare+Hospital+Veterinario)

---

## 📌 1. Visão Geral e Objetivo do Projeto

O **VetCare** é uma aplicação web institucional desenvolvida para simular um ambiente de desenvolvimento front-end profissional. O objetivo do projeto é oferecer uma interface moderna, acessível, responsiva e performática para tutores de animais de estimação que buscam atendimento médico especializado de urgência e consultas agendadas.

Este projeto foi construído com foco em **HTML5 semântico**, **CSS3 moderno** (sem o uso de frameworks externos), **separação rigorosa de responsabilidades** e alinhamento com os padrões do mercado (metodologia BEM, escala de fontes relativas e pontos de quebra fluídos).

---

## 🚀 2. Tecnologias e Conceitos Aplicados

* **HTML5 Semântico:** Uso de tags estruturais (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<details>`, `<summary>`, `<footer>`) para maximizar a acessibilidade e o SEO.
* **CSS3 Moderno & Design System:**
  * **Variáveis CSS (`:root`):** Padronização de cores, tipografia, sombras e raios de borda.
  * **Metodologia BEM (Block Element Modifier):** Nomenclatura clara e modular de classes e seletores CSS.
  * **Flexbox:** Construção da estrutura principal do layout e dos componentes de cards.
  * **CSS Fixed Positioning:** Implementação de menu lateral fixo, rodapé fixo e botão flutuante de atalho do WhatsApp.
* **Escala Relativa & Tipografia Proporcional:**
  * Redimensionamento da escala base no elemento `:root` (`html { font-size: 62.5%; }` ou equivalente).
  * Uso estrito da unidade `rem` para tipografia, espaçamentos (`margin`, `padding`) e bordas.
  * Uso de porcentagens (`%`) e unidades relativas à viewport (`vh` / `vw`) para responsividade fluida.
* **Google Fonts:** Importação e utilização da família de fontes **Poppins** (pesos 400, 500, 600 e 700).
* **Acessibilidade e Microinterações:**
  * Estados interativos (`:hover`, `:focus`) com transições suaves (`transition`) e animações de elevação (`box-shadow`, `transform`).
  * Rolagem suave nativa (`scroll-behavior: smooth`).
* **Integração externa:** API do WhatsApp para redirecionamento direto de contato.

---

## 📁 3. Organização da Arquitetura de Arquivos

A estrutura do projeto segue estritamente a separação de responsabilidades (RNF04), sem o uso de estilos *inline* ou blocos `<style>` dentro do arquivo HTML.

```text
vetcare-hospital/
│
├── index.html                # Estrutura principal da aplicação em HTML5 semântico
│
├── css/
│   ├── variables.css         # Variáveis globais (Tokens do Design System: cores, fontes, sombras)
│   ├── reset.css             # Reset de estilos e configuração do font-size base no :root
│   ├── style.css             # Estilos e posicionamento dos componentes BEM (Cards, Botões, FAQ, Flutuante)
│   └── responsive.css        # Media queries para adaptação em Mobile, Tablet e Desktop
│
├── assets/
│   └── img/                  # Imagens e ícones utilizados no projeto
│
└── README.md                 # Documentação completa do projeto
```

---

## 🛠️ 4. Instruções de Visualização e Execução

Para visualizar ou rodar este projeto localmente na sua máquina, siga os passos abaixo:

### Pré-requisitos
* Um navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).
* Extensão **Live Server** (recomendada caso utilize o VS Code).

### Passos para Execução:
1. **Clonar o Repositório:**
   ```bash
   git clone https://github.com/seu-usuario/vetcare-hospital.git
   ```
2. **Navegar até o diretório do projeto:**
   ```bash
   cd vetcare-hospital
   ```
3. **Abrir a Aplicação:**
   * **Opção 1:** Dê um duplo clique no arquivo `index.html` para abri-lo diretamente no seu navegador padrão.
   * **Opção 2 (Recomendada):** Abra a pasta do projeto no **VS Code**, clique com o botão direito no arquivo `index.html` e selecione **"Open with Live Server"**.

---

## 💡 5. Principais Desafios Técnicos e Aprendizados

1. **Arquitetura de Layout com Menu Fixo:**
   * **Desafio:** Manter o menu fixo à esquerda (`position: fixed`) no Desktop sem sobrepor o conteúdo das seções durante a rolagem, e garantir que a rolagem suave (`scroll-behavior: smooth`) pare no ponto exato da âncora.
   * **Solução:** Aplicação de margens esquerdas adequadas no container principal (`<main>`) para compensar a largura do menu fixo e ajuste das propriedades de recuo e `scroll-margin-top` nas seções.

2. **Adoção Rígida da Escala REM e Metodologia BEM:**
   * **Desafio:** Abandonar o uso habitual de pixels (`px`) em favorecimento absoluto de unidades `rem` e manter uma convenção BEM padronizada em todos os componentes.
   * **Solução:** Configuração do tamanho da fonte raiz em `62.5%` (onde `1rem = 10px`), facilitando a conversão e garantindo acessibilidade para usuários que alteram o tamanho de fonte padrão do navegador.

3. **Responsividade Fluida e Componentes Nativos:**
   * **Desafio:** Implementar um componente de FAQ expansível sem o auxílio de código JavaScript e adaptar o layout desktop de tela cheia para telas de dispositivos móveis.
   * **Solução:** Utilização das tags semânticas `<details>` e `<summary>` estilizadas via CSS e criação de *breakpoints* estratégicos utilizando *media queries* recomendadas pelo W3Schools.

---

### 📄 Licença e Informações Institucionais
* **Projeto:** Desenvolvimento Front-end - Turma B
* **Cliente Fictício:** VetCare Hospital Veterinário
* **Escola:** SENAI Henrique Lupo
* **Ano:** 2026