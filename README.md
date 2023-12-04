# 5586_project

Ótimo! Se o frontend já está pronto, agora você pode focar na integração com o backend e na implementação dos recursos específicos solicitados. Aqui estão alguns passos e considerações para continuar:

### 1. **Integração com o Backend:**
   - Utilize a documentação do Swagger para entender as endpoints e os métodos disponíveis no backend.
   - Configure as requisições HTTP (GET, POST, PUT, DELETE) conforme necessário para interagir com o backend.

### 2. **Autenticação e Armazenamento de Token:**
   - Implemente a autenticação do usuário utilizando os métodos no endpoint `/usuario/*`.
   - Após a autenticação, armazene o token e outras informações relevantes (como se o usuário é administrador) no storage local do navegador.

### 3. **Menu Superior e Nome do Usuário:**
   - Exiba o menu superior na tela principal com a opção "Países".
   - Mostre o nome do usuário na parte superior da tela, utilizando as informações obtidas na resposta da autorização.

### 4. **Tela de Consulta/Edição de Países:**
   - Desenvolva a tela de consulta/edição de países.
   - Implemente a lógica para permitir editar/excluir/incluir países apenas se o usuário for administrador.

### 5. **Tabela Paginada com Ordenação:**
   - Exiba a lista de países em uma tabela paginada.
   - Implemente a paginação no cliente e a ordenação também no cliente.

### 6. **Validações dos Campos:**
   - Implemente as validações adequadas nos campos, como a validação da sigla do estado.
   - Garanta que mensagens de erro sejam apresentadas ao usuário de maneira clara e amigável.

### 7. **Renovação Automática do Token:**
   - Antes de cada requisição, verifique se o token está próximo de expirar e o renove.
   - Trate os retornos 401 do backend para reautorizar o token automaticamente, tornando o processo transparente ao usuário.

Lembra de que a qualidade do código e a usabilidade da interface são aspectos essenciais na avaliação do resultado
