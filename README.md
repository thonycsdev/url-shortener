# Url Shortener

Aplicativo web para encurtar a URL de qualquer url da web. :)




## Stack utilizada

**Front-end:** React, Next.JS, TailwindCSS

**Back-end:** C#, .NET Framework, MongoDB


## Apêndice

O projeto foi idealizado seguindo a ideia de um encurtador de URL que seria contruido com um banco de dados relacional `Postgres`, porém decidi colocar a prova o design pattern de repository. Fiz a substituição do `EF Core` e do `Postgres` pelo `MongoDB` apenas. 

O impressionante foi que o pattern se manteve e que a aplicação se manteve consistente pois apenas depêndia da interface `IRepository<T>`. Mudando a implementação da interface e criando novos testes, foi possível manter todas as funcionalidades e regras de negócio intactas!.





## Rodando localmente

Clone o projeto

```bash
  git clone https://github.com/thonycsdev/url-shortener.git
```

Entre no diretório do projeto

```bash
  cd url-shortener
```

Instale as dependências de ambas stacks

```bash
  npm install && dotnet restore
```

Suba o container do docker compose com o mongoDB

```bash
  docker compose -f infra/compose.yml up
```

Inicie as stacks

```bash
  dotnet run && npm run start
```

