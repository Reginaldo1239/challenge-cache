# Challenge

Olá Developer,

Esse é o desafio da iUPay para desenvolvedores participando do nosso processo de contratação, não acreditamos em solução perfeita, apenas precisamos entender como você aborda problemas de software.

## Sobre o problema

Você foi contratado por uma empresa de pagamentos eletrônicos para melhorar a performance de uma API que precisa consultar o saldo do usuário.

Assuma que a solução atual é básica e conta com apenas uma API que escreve e lê transações que afetam o saldo do usuário diretamente no banco de dados. Atualmente a mesma API calcula o saldo de cada usuário e serve para um aplicativo móvel.

A cada pedido de consulta de saldo a solução existente está somando todas as transações do usuário em questão e apresentando o saldo. Este processo está demorando vários segundos e sua missão é propor uma solução melhor.

### O modelo de dados

Atualmente o banco de dados contém as seguintes colunas:
 - id_transacao (string)
 - id_usuario (string)
 - timestamp (int)
 - valor (double - positivo ou negativo)

Ao chamar a API /user/<user_id>/balance (GET), o sistema faz uma query na tabela acima filtrando todas as transações para <user_id>. Após isso o sistema retorna a soma do campo valor.

Sua missão é implementar uma aplicação que calcule o saldo de uma maneira melhor, utilizando a solução acima como base.

### O que esperamos de entregáveis

- [ ] Código do novo serviço GET /user/<user_id>/balance
- [ ] Fácil inicialização, sem muitos passos para poder da o start do projeto em qualquer ambiente (README).
- [ ] Criar testes de acordo com a necessidade do produto.
- [ ] Criar IaC (infraestructure as code), pode acontecer de sugir um cliente novo e precisamos subir um novo ambiente em qualquer outro lugar que seja.
- [ ] Definir um padrão de código e explicar em algum documento junto ao source code do projeto.
- [ ] Criar um CI CD para seu projeto usando GitHub Actions.

### Documentação da API

A maioria dos nossos cliente possuem uma área de tecnologia logo precisamos ter uma documentação bem estruturada da API.

### O que será testado?

1. Verificaremos todo o workflow criado para o projeto no GitHub Actions.
2. Usaremos o IaC do projeto para roda o mesmo em uma VM localmente.
3. Requisitaremos todos os recursos de acordo com a documentação criada.
4. Olharemos o padrão de código e a semântica dos testes criados.

**Obs:** Outros testes poderão surgir de acordo de como será a experiência com a solução criada.

### Como iniciar o desenvolvimento?

- [ ] Criar um fork para sua conta pessoal deste mesmo repositório e incluir no seu repositório pessoal os usuários @guiferpa e @lucasbmiguel
- [ ] Desenvolva toda a solução em seu repositório
- [ ] Por final faça o merge do seu projeto para um branch com o seu username do GitHub e abra uma issue assinalando o término do seu projeto. Caso necessário iremos pontua algumas coisas pela thread da issue antes mesmo de baixa o código pra teste.

### Considerações finais

Bom, é isso. Qualquer dúvida pode enviar para guilherme.paixao@iupay.com.br ou lucas.bonatto@iupay.com.br
