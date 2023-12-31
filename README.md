# Vulp API

Esta API fornece informações sobre jogadores do Minecraft, incluindo avatares, cabeças, corpos, skins e capas.

## Como Usar

### Endpoint
https://vulpapi.squareweb.app/minecraft/:username

### Exemplo de Solicitação com Axios (Node.js)

```javascript
const axios = require('axios');

const username = 'NomeDoJogador';

axios.get(`https://vulpapi.squareweb.app/minecraft/${username}`)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.error(error.response.data);
  });
```
### Exemplo de Solicitação com Node-Fetch (Node.js)

```javascript
const fetch = require('node-fetch');

const username = 'NomeDoJogador';

fetch(`https://vulpapi.squareweb.app/minecraft/${username}`)
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.error(error);
  });
```

### Resposta de Sucesso

```javascript
{
  "status": "success",
  "response": {
    "mcAvatar": "https://crafatar.com/avatars/UUID",
    "mcHead": "https://crafatar.com/renders/head/UUID",
    "mcBody": "https://crafatar.com/renders/Body/UUID",
    "mcSkins": "https://crafatar.com/skins/UUID",
    "mcCape": "https://crafatar.com/renders/capes/UUID"
  }
}
```

### Erro: Usuário não encontrado

```javascript
{
  "status": "error",
  "message": "Usuário não encontrado"
}
```

### Erro: Limite de Solicitações Atingido

```javascript
{
  "status": "error",
  "message": "Limite de solicitações atingido. Aguarde um momento e tente novamente."
}
```

### Erro: Nome de Jogador Inválido

```javascript
{
  "status": "error",
  "message": "Nome de jogador inválido"
}
```


### Erro: Não Autorizado

```javascript
{
  "status": "error",
  "message": "Não autorizado a acessar as informações do jogador."
}
```

### Erro Interno na API

```javascript
{
  "status": "error",
  "message": "Erro interno na API"
}
```


