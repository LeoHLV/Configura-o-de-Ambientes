# Definir uma versão dotnet via JSON
Crie a .sln no mesmo local do arquivo JSON para atribuir a versão

- Verificar Versões<br>
`dotnet --list-skds`

- Criar json com versão<br>
`dotnet new globaljson --sdk-version 6.0.401`

# Criando Web API

- Cria uma solution limpa para o projeto<br>
`dotnet new sln -n NomeDaSolution`

- Criar aplicação principal Web API<br>
`dotnet new webapi -n WebAPI -o API.WebAPI`

- Criar LIBs<br>
`dotnet new classlib -n Domain -o API.Domain`<br>
`dotnet new classlib -n Infra.Data -o API.Infra.Data`<br>
`dotnet new classlib -n Infra.IoC -o API.Infra.IoC`<br>
`dotnet new classlib -n Entities -o API.Application`

- **Vincular todas as LIBs a solution de uma vez**<br>
`dotnet sln add **/*.csproj`

- **Vincular LIBs a solution individualmente**<br>
`dotnet sln add ./API.WebAPI/`<br>
`dotnet sln add ./API.Domain/`<br>
`dotnet sln add ./API.Infra.Data/`<br>
` dotnet sln add ./API.Infra.IoC/`<br>
`dotnet sln add ./API.Application/`<br>

`dotnet build` : para verificar erros e gerar binários

>Abrir na .sln com VS-IDE clicar no webapi e marcar como principal

