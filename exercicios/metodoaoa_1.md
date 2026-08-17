# Rede AOA - Exercício 01

A rede AOA conecta atividades através de eventos, identificados numericamente, e que marcam o início e/ou fim de cada atividade. 

Cada atividade é simbolizada por uma seta, e identificada por uma letra, e um valor numérico, representando a sua duração. Note nas imagens que, a cada atividade iniciada, parte de um evento identificado, e aponta para outro evento (que ainda não foi identificado ainda).

Cada atividade iniciada é decorrente de outra atividade precedente, ou é marcada como atividade inicial da rede, como indicada como evento 1.
![alt text](image-6.png)
![alt text](image-7.png)
![alt text](image-8.png)
![alt text](image-9.png)
![alt text](image-10.png)
![alt text](image-11.png)
![alt text](image-12.png)
![alt text](image-13.png)
![alt text](image-14.png)
![alt text](image-15.png)
![alt text](image-16.png)
![alt text](image-17.png)

Após construção de todas as conexões da rede, resta verificar as atividades fictícias (ou fantasmas, ou dummies), indicadas em setas cinzas.

Quando temos dois eventos que apontam para uma única atividade, a atividade fictícia partirá de um dos eventos, e apontará para o outro, pois não podemos ter dois eventos que iniciam uma atividade ao mesmo tempo.

Assim, a escolha do evento que iniciará a atividade fictícia é pelo evento que possuir mais de uma atividade iniciada. Assim, a atividade vinculada a este evento que estava em análise será apagada, em substituição da atividade fictícia.


![alt text](image-18.png)
![alt text](image-20.png)
![alt text](image-21.png)

Ao concluir a última atividade identificada, temos então a rede AON montada com todas as conexões.

![alt text](image-22.png)

Analisando todos os caminhos, realizamos a soma de cada um, isoladamente. Aquele caminho que possuir a maior soma das atividades associadas a ele, será o caminho crítico. 

Note que se a rede possuir muitos caminhos, aumenta-se a quantidade de somas, tornando este processo muito trabalhoso.  

Destacamos em vermelho o caminho crítico, correspondente ao caminho de maior duração. Os caminhos não críticos estão identificados na cor cinza.

![alt text](image-23.png)
![alt text](image-24.png)

### Calculando o Data Cedo (TE)

O cálculo do TE sempre será do sentido da esquerda para a direita, até o evento 16.

O evento 1 sempre inicia com TE = 0. O TE dos eventos 2 e 3 utilizarão este valor, somando com a duração das atividades correspondentes aos seus eventos. 

Para cada atividade, o TE do evento anterior será somado com a duração da atividade, resultano no TE do evento seguinte. Observe que há caminhos que convergem para um mesmo evento, e o critério de prioridade é pelo valor de TE maior.


![alt text](image-25.png)

O cálculo para Data tarde (TL) faz o sentido inverso, realiza a subtração, e o critério de prioridade é pelo menor valor de TL.

![alt text](image-26.png)

Temos os dados de todos os eventos preenchidos, e os caminhos identificados.

![alt text](image-27.png)

Para a Folga Total e Folga Livre, seguimos a expressão mostrada na imagem. 

![alt text](image-28.png)

Temos então as folgas indicadas para cada atividade.

![alt text](image-29.png)

Outros tipos de folgas, em especial para a Folga do Evento, que delineia o caminho crítico.

![alt text](image-19.png)

Concluíndo, os valores de ES, EF, LF e LS. Para a Rede AON e a Rede AOA, os valores devem ser iguais.

![alt text](image-31.png)

![alt text](image-45.png)


