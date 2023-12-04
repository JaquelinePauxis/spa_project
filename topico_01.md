Vamos criar um exemplo básico para a integração do frontend com o backend. Lembre-se de adaptar isso de acordo com a estrutura e requisitos específicos do seu projeto. Vou apresentar um exemplo em JavaScript com o uso de `fetch` para as requisições HTTP:

### Exemplo de Integração com o Backend (JavaScript):

Suponha que você tenha um arquivo `api.js` responsável por lidar com as requisições ao backend:

```javascript
// api.js

const BASE_URL = 'http://localhost:8090'; // Altere conforme a URL do seu backend

export const loginUser = async (username, password) => {
  const response = await fetch(`${BASE_URL}/usuario/login`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ username, password }),
  });

  if (!response.ok) {
    throw new Error('Erro ao autenticar o usuário');
  }

  return response.json();
};

export const getPaises = async (token) => {
  const response = await fetch(`${BASE_URL}/paises`, {
    method: 'GET',
    headers: {
      'Content-Type': 'application/json',
      Authorization: `Bearer ${token}`,
    },
  });

  if (!response.ok) {
    throw new Error('Erro ao obter a lista de países');
  }

  return response.json();
};

// Adicione mais funções para editar, excluir e incluir países conforme necessário
```

Agora, no seu componente ou arquivo principal, você pode importar e usar essas funções:

```javascript
// main.js

import { loginUser, getPaises } from './api.js';

// Exemplo de uso
const username = 'seu_usuario';
const password = 'sua_senha';

try {
  const authResponse = await loginUser(username, password);
  const token = authResponse.token;

  // Salve o token e outras informações necessárias no storage local

  const paisesResponse = await getPaises(token);
  const paises = paisesResponse.paises;

  // Manipule a lista de países conforme necessário

} catch (error) {
  console.error(error.message);
}
```

Este é apenas um exemplo básico para ilustrar como você pode integrar o frontend com o backend. Lembre-se de tratar erros adequadamente, implementar a renovação do token e adicionar mais funcionalidades conforme necessário para atender aos requisitos do seu projeto.
