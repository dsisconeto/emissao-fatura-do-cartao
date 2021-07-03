# Emissão da fatura do cartão

Você deve desenvolver uma aplicação que faça a emissão da fatura do cartão de crédito, dado um cliente e mês da fatura.



## Arquitetura

Nossa aplicação iniciamente será uma CLI que aceita os parâmetros cliente e mês conforme o exemplo abaixo.

``java -jar meuprograma --cliente=1212 --mes=04``


### Valor:

Possibilitar o cliente ver a fatura detalhada para entender os seus gastos.

### Incremento

Emissão da fatura do cliente de forma detalhada.

### Verificação
 - A faturada emitida deve conter os seguintes dados:
   - O mês de referência.
   - _Id_ da fatura.
   - Data de fechamento.
   - Data de vencimento.
   - A melhor data para comprar.
   - Valor total que é a soma de todas as compras menos os descontos.
 - Cada compra da fatura deve conter:
   - Referência
   - Data
   - Descrição
   - Valor
 - A data de fechamento deve ser 10 dias antes do vencimento.  
 - Cliente com mais de 2 anos ganham desconto de 20%.
   - Se o cliente não tiver direito não deve ser apresentado
 - Quando não houver compras, deve apresentar a mensagem “Vamos gastar Mais”.
 - Deve exibir a mensagem “Não há fatura para o mês”, caso não tenha fatura para o cliente no mês informado.
 - Deve exibir a mensagem “Cliente não existe”, caso o cliente informado não exista.
   
### Exemplo para inspiração:

 <pre>
 Dejair Sisconeto conosco desde 08/04/2021
 Fatura de Janeiro
 Fechamento: 08/04/2021 | Vencimento: 08/04/2021 | Melhor data compra 07/04/2021
 Referencia | DATA   | DESCRIÇÃO                               | VALOR
 - 2121       19/02  | Descrição muito grande...               | R$ 2,00
 
 Desconto: R$ 20,00
 Total da fatura = R$ 20,30 
 TOTAL = 20,30

Cliente com mais de 2 anos ganha desconto de 20%.
</pre>
