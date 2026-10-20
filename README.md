# ♻️ ComPartilhe — Plataforma de Economia Solidária e Moda Circular

> **Aplicação web para gestão de feiras de troca, circulação de moedas sociais e acompanhamento de doações no Instituto Federal do Paraná (IFPR) - Câmpus Paranaguá.**

---

## 📌 Sobre o Projeto

O **ComPartilhe** é uma iniciativa de cunho social, ambiental e educacional desenvolvida no **Instituto Federal do Paraná (IFPR - Câmpus Paranaguá)**. Seu objetivo principal é combater os impactos socioambientais do *fast fashion* promovendo a **moda circular**, a **economia solidária** e o **consumo consciente**.

A aplicação web foi desenvolvida para digitalizar e otimizar a gestão das feiras de troca, substituindo o controle manual por uma plataforma centralizada capaz de:
- Gerenciar o acervo/estoque de peças doadas (roupas, calçados, livros, eletrônicos, etc.);
- Controlar o saldo de **créditos sociais** (moeda alternativa do clube de trocas);
- Registrar as transações de entrada e saída de itens de forma ágil e segura;
- Gerar histórico estruturado de dados para futuros estudos de mensuração de impacto ambiental (ex: créditos de carbono).

---

## 🚀 Tecnologias Utilizadas

O projeto foi modernizado e containerizado para fácil execução e implantação em qualquer ambiente.

* **Backend:** [PHP 8.2+](https://www.php.net/) / [Laravel Framework](https://laravel.com/)
* **Autenticação & Scaffolding:** [Laravel Jetstream](https://jetstream.laravel.com/) (Fortify / Sanctum)
* **Frontend:** [Blade Templates](https://laravel.com/docs/blade), [Tailwind CSS](https://tailwindcss.com/), [Bootstrap](https://getbootstrap.com/), [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
* **Banco de Dados:** [MySQL](https://www.mysql.com/)
* **Containerização:** [Docker](https://www.docker.com/) & [Laravel Sail](https://laravel.com/docs/sail)
* **Gerenciamento de Assets:** [Vite](https://vitejs.dev/)

---

## 🛠️ Como Executar o Projeto Localmente

### Pré-requisitos
* [Docker](https://docs.docker.com/get-docker/) e [Docker Compose](https://docs.docker.com/compose/install/) instalados na máquina.
* Git.

### Passo a Passo

1. **Clonar o repositório:**
   ```bash
   git clone [https://github.com/AlexandreH4564/compartilhe-tcc.git](https://github.com/AlexandreH4564/compartilhe-tcc.git)
   cd compartilhe-tcc

2. **Copiar o arquivo de variáveis de ambiente:**
   ```bash
   cp .env.example .env

3. **Subir os containers com o Laravel Sail:**
   ```bash
   ./vendor/bin/sail up -d

4. **Gerar a chave da aplicação:**
   ```bash
   ./vendor/bin/sail artisan key:generate

5. **Executar as migrações do banco de dados:**
   ```bash
   ./vendor/bin/sail artisan migrate

6. **Instalar e compilar as dependências do Frontend (Assets):**
   ```bash
    ./vendor/bin/sail npm install
    ./vendor/bin/sail npm run build

7. **Acessar a aplicação:**
   ```bash
   Abra o seu navegador e acesse: http://localhost

