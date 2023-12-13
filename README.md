# Minecraft API

Esta API fornece informações sobre jogadores do Minecraft, incluindo avatares, cabeças, corpos, skins e capas.

## Como Usar

### Endpoint
https:aa/minecraft/:username

### Exemplo de Solicitação com Axios (Node.js)

```javascript
const axios = require('axios');

const username = 'NomeDoJogador';

axios.get(`https://seu-domínio.com/minecraft/${username}`)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.error(error.response.data);
  });
```

```javascript
const fetch = require('node-fetch');

const username = 'NomeDoJogador';

fetch(`https://seu-domínio.com/minecraft/${username}`)
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.error(error);
  });
```





