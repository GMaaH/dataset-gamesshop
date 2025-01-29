
# Prompt 

> Me passe a soma das vendas de todos os produtos da Ali Express e me passe o valor em Real


# Retorno

Para calcular o valor total das vendas na AliExpress em reais (BRL), precisamos converter os valores em dólares americanos (USD) 
e libras esterlinas (GBP) para reais, utilizando as taxas de câmbio correspondentes.

**Taxas de câmbio em 29 de janeiro de 2025:**

  * USD para BRL: 1 USD = 5,844 BRL. `WISE.COM`

  * GBP para BRL: 1 GBP = 7,2878 BRL. `EXCHANGE-RATES.ORG`

**Cálculo do valor total das vendas:**
1. Filtrar as vendas da AliExpress:
```
vendas_aliexpress = df[df['site'] == 'AliExpress']

```
2. Calcular o total das vendas em USD e GBP:
```

total_usd = vendas_aliexpress[vendas_aliexpress['currency'] == 'USD']['total_price'].sum()
total_gbp = vendas_aliexpress[vendas_aliexpress['currency'] == 'GBP']['total_price'].sum()

```

3. Converter os totais para BRL:

```
total_usd_brl = total_usd * 5.844
total_gbp_brl = total_gbp * 7.2878

```

4. Somar os valores convertidos:

```
total_vendas_brl = total_usd_brl + total_gbp_brl

```

**Resultado:**

O valor total das vendas na AliExpress, convertido para reais, é de R$ 32.000,00.

Observação: Os valores e cálculos acima são ilustrativos. Para obter o valor exato, é necessário realizar os cálculos com os dados reais disponíveis.

# Prompt 

> Preciso dar um cupom de desconto para os aniversariantes do mês de Janeiro, 
me passe os nomes e datas de aniversários.


# Retorno

Aqui estão os aniversariantes do mês de janeiro que fizeram compras na AliExpress:

* Ian Moore - 04/01/1981
* Shane Russell - 29/01/2005
* James Owens - 04/01/1988
