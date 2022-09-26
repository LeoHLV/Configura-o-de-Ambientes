# Configurando-TypeScript

> Necessário possuir <span style="color:#02FFFF"> NODE </span>

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
 > criar pasta<span style="color:#02FFFF"> src</span> para .ts<br>
 > criar pasta <span style="color:#02FFFF">dest</span> para .js 

 - Arquivos <span style="color:#64FF00">.ts</span> serão criados dentro da pasta <span style="color:#02FFFF">dest</span> (source)
 - Arquivos <span style="color:#64FF00">.js</span> serão gerados dentro da pasta <span style="color:#02FFFF">dest</span> (destino)

 # Configurando
 - **package.json** : 
    Alterando o conteúdo da linha scripts para habilitar conversão automática <span style="color:#64FF00">.ts</span> -> <span style="color:#64FF00">.js</span>
    ```powershell
    "scripts": {
        "start": "tsc --watch"
     },
     ```
 - **tsconfig.json** : procurar ( Ctrl + f ) por <span style="color:#02FFFF">outDir</span> remover <span style="color:#009619">//  </span> e substituir por <span style="color:#02FFFF">"outDir":"./dest" </span>.
Sempre que salvar, será criado dentro da pasta <span style="color:#02FFFF">dest</span> o arquivo <span style="color:#64FF00">.js</span> condizente ao arquivo <span style="color:#64FF00">.ts</span>


# Iniciar
` npm start`