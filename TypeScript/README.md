# Configurando-TypeScript

> Necessário possuir NODE

- Instalar Globalmente<br>
`npm install -g typescript`

- verificar versão <br>
`tsc -v`

# Adicionar ao projeto

 - Gerar package.json<br>
`npm init -v`

 - Gerar node_modules e criar package.json <br>
`package-lock.json`

 - Gerar tsconfig.json <br>
`npx tsc --init`

 # Organizando <br>
 > criar pasta src para .ts<br>
 > criar pasta dest para .js 

 - Arquivos .ts serão criados dentro da pasta src (source)
 - Arquivos .js serão gerados dentro da pasta dest (destino)

 # Configurando
 - **package.json** : 
    Alterando o conteúdo da linha scripts para habilitar conversão automática .ts -> .js
    ```powershell
    "scripts": {
        "start": "tsc --watch"
     },
     ```
 - **tsconfig.json** : procurar ( Ctrl + f ) por outDir,  remover // e substituir por "outDir":"./dest". Sempre que salvar, será criado dentro da pasta dest o arquivo .js condizente ao arquivo .ts


# Iniciar
` npm start`