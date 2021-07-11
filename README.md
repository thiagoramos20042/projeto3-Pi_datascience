# Projeto módulo 3

Sistema de consumo de cartão de crédito

Você e todas de sua equipe começaram a trabalhar em uma empresa fornecedora de crédito que acabou de iniciar suas atividades. O único produto da empresa, por enquanto, é um cartão de crédito. Nos últimos meses, a empresa se dedicou à captação de clientes, e em janeiro de 2021, conta com uma pequena mas ativa base de 20 clientes!

Para cada um dos 20 clientes foi liberado um limite de crédito, definido no momento da solicitação do cartão. O limite de cada cliente está cadastrado em uma base de dados.

Assim que eles receberam o cartão, os clientes começaram a utilizá-lo para fazer compras (algumas delas parceladas), e todas estas compras foram registradas em uma outra base de dados.

No entanto, apesar de haver estas duas bases de dados, elas não conversam entre si, o que implica em um grande problema: não é possível saber que clientes gastaram dentro do limite, e quais eventualmente já gastaram mais que o limite!

E esse é o primeiro projeto da equipe na empresa: elaborar um processo em Python que leia os dados disponíveis, os processe, e no final disponibilize um relatório que mostre qual é o limite de cada cliente, e em quanto está a fatura em cada um dos meses de 2021. 

Se houver algum caso de estouro de limite, você deve indicar no relatório com um destaque em vermelho, para garantir maior tempestividade de ação nestes casos.

No primeiro passo do projeto, você não precisa montar o relatório completo: basta gerar uma tabela (em forma de imagem colorida!), que contenha as informações acima. A tabela a ser gerada está na pasta, com título relatorio_consumo. Este é o principal output.

Em resumo, temos:

inputs: arquivo gastos_limites.xlsx, que contém duas sheets:
- sheet "gastos": base com as compras dos clientes. Cada linha se refere a uma única operação, e é caracterizada pelas colunas de: nome do cliente que realizou a operação; valor da operação; número de vezes em que a compra foi parcelada; a data em que a compra foi realizada; o mês atual. Nesta base há apenas operações referentes a janeiro de 2021;
- sheet "limites": base de cadastro de limites de cada um dos clientes. Cada linha se refere a um cliente, e é dada pelas colunas de: nome do cliente; valor do limite de crédito do cartão; data de fechamento da fatura.

outputs: uma imagem o mais próxima possível da imagem relatorio_consumo.png, na pasta. Como os dados utilizados foram os mesmos, os dados na tabela devem ser os mesmos. E, idealmente, a formatação deve ser exatamente igual. Caso isso não seja possível, pode haver variações na formatação, mas o resultado final deve obrigatoriamente ser uma tabela renderizada em imagem, com os seguintes elementos:
- Uma linha referente a cada cliente;
- As seguintes colunas: nome do cliente; valor do limite de crédito daquele cliente; valor de cada uma das faturas, de janeiro até dezembro de 2021;
- Valores numéricos formatados em notação monetária brasileira (R$ XX.XXX,XX);
- Indicação em vermelho das faturas que representam estouro de limite, e também dos nomes dos clientes que tiveram no mínimo um estouro.

___________

Observações adicionais/dicas:

- O valor de cada fatura deve ser calculado unicamente utilizando os dados de operações que estão na sheet "gastos", que se referem a operações realizadas em janeiro/2021, mas que podem ter sido parceladas -- daí a possibilidade de saldo em faturas futuras.
- Se atente à data de fechamento da fatura e à sua relação com a fatura de janeiro!
- Caso sobre tempo, sinta-se à vontade para fazer mais coisas além do que foi pedido! (talvez fazer alguma análise exploratória da base, ou gerar o relatório em PDF contendo a imagem da tabela?)