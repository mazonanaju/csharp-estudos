# Anotações C-SHARP
C# é uma linguagem orientada a objetos de programação de alto nivel(sintaxe mais proxima a linguagem humana).

Objetivo: Simples e econômico.


.NET é uma plataforma com bibliotecas e classes prontas.

- .NET framework (only windows)

- .NET core (windows, linux & mac)

- .NET versão mais atualizada

 

-----------------------------------------------------------------------------------------------------

# POO - paradigma de programação que coloca OBJETOS como elementos centrais no desenvolvimento.

 

- DADOS ou ATRIBUTOS: informaçãoes a respeito do objeto

- FUNÇÕES ou METODOS: Ações do objeto

 

HERANÇA: permite uma hierarquia de classes (EX: Veiculo - Carro, Onibus...)

ENCAPSULAMENTO: acesso (public, internal, private, protected)

ABSTRAÇÃO: classes abstratas

POLIMORFISMO: métodos com diferentes comportamentos em classes derivadas de uma base

-----------------------------------------------------------------------------------------------------

# API recebe uma chamada de um outro software e devolve uma resposta.

Interoperabilidade: Não se importa com a linguagem de programação que está chamando.

Comunicação através de HTTP, na maioria dos casos em formato json.

Funcionalidades: é um recurso(ENDPOINT) para cada funcionalidade tem um ENDPOINT.
Métodos: Post(criando), Put(atualizando), Delete(apagando) & Get(recuperando).

COMMANDS:

# Inicializar e executar projetos
- dotnet run                                       # Executa o projeto atual
- dotnet new webapi -n NomeDaApi                   # Cria uma nova API Web
- dotnet new console                               # Cria um projeto executável (console)
- dotnet new classlib -n NomeDaBiblioteca          # Cria uma biblioteca de classes

# Gerenciamento de soluções e referências
- dotnet new sln                                   # Cria uma solução para agrupar projetos
- dotnet sln add [caminho_do_projeto.csproj]       # Adiciona projeto à solução
- dotnet add reference [caminho_do_projeto.csproj] # Adiciona referência entre projetos

# Pacotes e dependências
- dotnet add package Swashbuckle.AspNetCore        # Instala o Swagger para documentação
- dotnet restore                                   # Restaura pacotes NuGet
- dotnet clean                                     # Limpa arquivos temporários/build
- dotnet build                                     # Compila o projeto (verifica erros)

# Fluxo
- dotnet new webapi -n MinhaApi
- dotnet new classlib -n MinhaBiblioteca
- dotnet new sln
- dotnet sln add MinhaApi/MinhaApi.csproj
- dotnet sln add MinhaBiblioteca/MinhaBiblioteca.csproj
- dotnet add MinhaApi/MinhaApi.csproj reference MinhaBiblioteca/MinhaBiblioteca.csproj
- dotnet add MinhaApi package Swashbuckle.AspNetCore
- dotnet build
- dotnet run --project MinhaApi

- Dica: dotnet --help mostra todos os comandos

- namespace: endereço - Projeto.NomedaPasta
- using Microsoft.AspNetCore.Mvc;
→ É uma diretiva de importação que disponibiliza ferramentas para construir APIs e aplicações web no ASP.NET Core.

Funcionalidade principal:
→ Fornece classes e atributos essenciais para implementar o padrão MVC (Model-View-Controller).

Recursos habilitados por essa importação:

[ApiController]: Transforma uma classe em um controlador de API.

[Route]: Define o caminho da URL para acessar endpoints.

[HttpGet], [HttpPost], etc.: Especificam métodos HTTP (GET, POST, etc.).

ControllerBase: Classe base que oferece métodos úteis como Ok(), NotFound(), BadRequest().
# Controller

    [ApiController]
    [Route("[controller]")] - rota

