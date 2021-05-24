# Impressão da fatura do cartão

Você deve desenvolver uma CLI que imprima no _stdout_ a fatura do cartão de crédito, passando o _id_ do cliente
e o mês da fatura.
Os dados vão está nos arquivos json.

### Valor:

Possibilitar o cliente ver a fatura detalhada para entender os seus gastos.

### Incremento

Imprimir a fatura do cliente de forma detalhada no _stdout_.

### Verificação

 - Deve conter o mês de referência.
 - Deve conter _id_ da fatura.
 - Deve conter a data de fechamento.
 - Deve conter a data de vencimento.
 - Deve conter a melhor data para comprar.
 - Deve imprimir a mensagem “Não há fatura para o mês”, caso não tenha fatura para o cliente no mês informado.
 - Deve imprimir a mensagem “Cliente não existe”, caso o cliente informado não exista.
 - A data de fechamento deve ser 10 dias antes do vencimento.  
 - Deve conter o valor total que é a soma de todas as compras menos os descontos.
 - Cliente com mais de 2 anos ganham desconto de 20%.
   - Se o cliente não tiver direito não deve ser apresentado.
 - Quando não houver compras, deve apresentar a mensagem “Vamos gastar Mais”.
 - Cada compra da fatura deve conter:
   - Referência
   - Data
   - Descrição
   - Valor
   
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


### Links.

- https://gradle-pitest-plugin.solidsoft.info/
- https://www.codurance.com/publications/2020/01/27/minimum-valuable-increment
- https://www.codurance.com/publications/2017/10/23/outside-in-design
- https://philcalcado.com/2010/12/23/how_to_write_a_repository.html
- https://xp123.com/articles/3a-arrange-act-assert