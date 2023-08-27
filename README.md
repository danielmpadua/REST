# REST

Study on REST and RESTful

## RESTful

RESTful é a aplicação dos padrões REST que são:

- _Uniform Interface_: Manter uma uniformidade, uma constância, um padrão na construção da interface. Nossa API precisa ser coerente para quem vai consumi-lá. Precisa fazer sentido para o cliente e não ser confusa. Logo, coisas como: o uso correto dos verbos HTTP; endpoints coerentes (todos os endpoints no plural, por exemplo); usar somente uma linguagem de comunicação (json) e não várias ao mesmo tempo; sempre enviar respostas aos clientes; são exemplos de aplicação de uma interface uniforme.

- _Client-server_: Separação do cliente e do armazenamento de dados (servidor), dessa forma, poderemos ter uma portabilidade do nosso sistema, usando o React para WEB e React Native para o smartphone, por exemplo.

- _Stateless_: Cada requisição que o cliente faz para o servidor, deverá conter todas as informações necessárias para o servidor entender e responder (RESPONSE) a requisição (REQUEST). Exemplo: A sessão do usuário deverá ser enviada em todas as requisições, para saber se aquele usuário está autenticado e apto a usar os serviços, e o servidor não pode lembrar que o cliente foi autenticado na requisição anterior. Nos nossos cursos, temos por padrão usar tokens para as comunicações.

- _Cacheable_: As respostas para uma requisição, deverão ser explicitas ao dizer se aquela resquição, pode ou não ser cacheada pelo cliente.

- _Layered System_: O cliente acessa a um endpoint, sem precisar saber da complexidade, de quais passos estão sendo necessários para o servidor responder a requisição, ou quais outras camadas o servidor estará lidando, para que a requisição seja respondida.

- _Code on demand (optional)_: Dá a possibilidade da nossa aplicação pegar códigos, como o javascript, por exemplo, e executar no cliente.

## Boas práticas

- Utilizar verbos HTTP para realizar requisições
- Manter um padrão na criação dos endpoints (singular ou plural)
- Não deixar barra no final do endpoint
- Nunca deixe o cliente sem resposta

## Verbos HTTP

- GET: Receber dados de um Resource
- POST: Enviar dados para serem processador por um Resource
- PUT: Atualizar dados de um Resource
- DELETE: Deeletar um Resource

## Status das Respostas

- 1xx: Informação
- 2xx: Sucesso
  - 200: OK
  - 201: CREATED
  - 204: Não tem conteúdo PUT POST DELETE
- 3xx: Redirection
- 4xx: Cliente Error
  - 400: Bad Request
  - 404: Not Found
- 5xx: Server Error
  - 500: Internal Server Error
