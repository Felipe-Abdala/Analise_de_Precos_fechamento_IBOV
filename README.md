**Análise de Preços de fechamento do Ibovespa**
**Pós-Tech Data Analytics**<br/>
**Turma:** 5DTAT<br/>
**Grupo:** 65<br/>

<br/>

**Membros do grupo**

| Integrantes                        | RM              |
| ---------------------------------- | --------------- |
| Felipe David Abdala                | RM355751        |
| Lucas Cardoso de Oliveir           | RM354959        |
| Natanael Amaro Honório dos Santos  | RM355375        |

<br/>

**Objetivo:**<br/>

> Neste notebook é exposta a série temporal de preços do IBOVESPA, durante 34 anos, compreendendo o período de 01/01/1990 à 15/07/2024. Posteriormente tratatada, para contemplar apenas de 01/01/2000 à 15/07/2024. <br/>
Com o intuito de testar modelos estatísticos que prevejam com acuracidade qual o preço de fechamento do índice da bolsa de valores brasileira (B3), o IBOVESPA.

<br/>

**Diretório:**<br/>
> O diretório do Git-hub com os scripts é o seguinte:
https://github.com/Felipe-Abdala/Tech_Challenge_Fase2

<br/>

**Metodologia:**<br/>

> Foram utilizados modelos de predição a fim de detectar qual melhor se adequaria para fins de previsão do valor de fechamento da bolsa brasileira (B3), com isso, foram utiilzadas as técnicas de modelagem de:
* Modelo Status Forecast (baseline, sazonalidade e base móvel);
* ARIMA;
* XGBoost;
* Prophet;
* SARIMAX.




> Todos os modelos apresentaram resultados parecidos, seja de acuracidade, seja de seus erros, com exceção do Prophet, que apresentou níveis de acuracidade menores que dos demais e também apresentou métricas de erro também maiores que dos demais modelos.
</br>

> Com isso, o MAE e do MAPE, conforme bibliografia suporte corrobora (https://medium.com/data-hackers/prevendo-n%C3%BAmeros-entendendo-m%C3%A9tricas-de-regress%C3%A3o-35545e011e70), são técnicas que não são tão afetadas por valores discrepantes e possuem melhor interpretabilidade de seus resultados para fins de entendimento da divergência entre o previsto e o observado. E a partir dessas duas técnicas (MAE e o MAPE) observou-se 4 modelos que melhor performaram: ***XGBoost, Sarimax, AutoArima e Naive.***
</br>

> Foram utilizados dados da B3, desde 01/01/2000 até 15/07/2024, após filtrarmos dados apenas a partir do ano 2000, já que é onde há maiores detalhamento dos anos com os dados de cotação da B3, de maneira mais robusta.
</br>

> Em resumo, a nossa melhor taxa de acerto é menor média de erro quadrado, foi na utilização do modelo **XGBoost** entendendo melhor o modelo. A seguir, seguem os pontos do porquê de esse modelo se mostrar aderem ao propósito das predições almejadas para a tomada de decisão de escolha final:</br>
>- O modelo apresenta uma facilidade para lidar com dados faltantes na base de dados, não enviesando o modelo final.
>- ⁠O modelo trabalha com um conceito de árvore de decisão, o que permite que esses outliers que podem faltar não influenciem no lado tomado pelo modelo.

**Conclusão:**</br>
>O modelo (XGBoost) se mostrou com os melhores indicadores, pelo fato de trabalhar melhor com séries temporais, e consequentemente a base de dados fornecida e trabalhada ser uma série temporal. E com isso, a base de teste teve seus dados previstos mais aderentes com a base de treino, quando comparamos no gráfico do modelo do XGBoost (vide navegação desse script no índice "***7.2.2.3. Avaliação do Modelo XGBoost***".
</br></br>

