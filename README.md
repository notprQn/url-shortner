# URL Shortener API

Esta é uma aplicação de encurtador de URL construída usando o framework Fiber em Go. A aplicação permite encurtar URLs longas e resolver URLs encurtadas.

## Sumário

- [Instalação](#instalação)
- [Uso](#uso)
- [Rotas da API](#rotas-da-api)
- [Variáveis de Ambiente](#variáveis-de-ambiente)
- [Contribuição](#contribuição)

## Instalação

Para instalar e executar esta aplicação localmente, siga os passos abaixo:

1. Clone o repositório:

    ```sh
    git clone https://github.com/seu-usuario/url-shortener.git
    cd url-shortener
    ```

2. Instale as dependências:

    ```sh
    go mod download
    ```

3. Crie um arquivo `.env` na raiz do projeto e defina a variável de ambiente `APP_PORT`:

    ```sh
    echo "APP_PORT=:3000" > .env
    ```

4. Execute a aplicação:

    ```sh
    docker-compose up -d
    ```

## Uso

Uma vez que a aplicação estiver em execução, você pode usar as seguintes rotas para encurtar URLs e resolver URLs encurtadas.

## Rotas da API

### `POST /api/v1`

Esta rota é usada para encurtar uma URL longa.

- **Request:**

    ```json
    {
        "url": "https://www.exemplo.com"
    }
    ```

- **Response:**

    ```json
    {
        "short_url": "http://localhost:3000/abcd1234"
    }
    ```

### `GET /:url`

Esta rota é usada para resolver uma URL encurtada.

- **Request:**

    - `:url` é o código da URL encurtada.

- **Response:**

    A resposta será um redirecionamento para a URL original.

## Variáveis de Ambiente

- `APP_PORT`: Define a porta em que a aplicação irá rodar (exemplo: `:3000`).

## Contribuição

1. Faça um fork do repositório.
2. Crie uma nova branch (`git checkout -b feature/nova-feature`).
3. Faça suas modificações e commit (`git commit -am 'Adiciona nova feature'`).
4. Envie para o branch (`git push origin feature/nova-feature`).
5. Crie um novo Pull Request.
