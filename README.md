# CodePix

### Sobre o projeto:
- É uma solução parar simularmos transferências de valores entre bancos fictícios através de chaves (e-mail e CPF);
- Simularemos diversos bancos e contas bancárias que possuem uma chave Pix atribuída;
- Cada conta bancária poderá cadastrar suas chaves Pix;
- Uma conta bancária poderá realizar uma transferência para outra conta em outro banco utilizando a chave Pix da conta de destino;
- Uma transação não pode ser perdida mesmo que: o CodePix esteja fora do ar;
- Uma transação não pode ser perdida mesmo que: o Banco de destino esteja fora do ar.

### Sobre os bancos:
- O banco será um microserviço com funções limitadas a cadastro de contas e chaves Pix, bem como transferência de valores;
- Utilizaremos a mesma aplicação parar simularmos diversos bancos, mudando apenas cores, nome e código;
- Nest.js no backend;
- Next.js no frontend.

### Sobre o CodePix:
- O microserviço CodePix será responsável por intermediar as transferências bancárias;
- Receberá a transação de transferência;
- Encaminhará a transação para o banco de destino (Status: "pending");
- Recebe a confirmação do banco de destino (Status: "confirmed");
- Envia confirmação para o banco de origem informado quando o banco de destino processou;
- Recebe a confirmação do banco de origem de que ele processou (Status: "completed");
- Marca a transação como completa (Status: "completed").
