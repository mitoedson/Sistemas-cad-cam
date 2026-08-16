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

Analisando todos os caminhos, realizamos a soma de cada um, isoladamente. Aquele caminho que possuir a maior soma das atividades associadas a ela, será o caminho crítico. 

Note que se houver muitos caminhos, teremos muito mais trabalho identificar qual o caminho crítico devido a quantidade de possibilidades para soma.

![alt text](image-23.png)
![alt text](image-24.png)
![alt text](image-25.png)
![alt text](image-26.png)
![alt text](image-27.png)
![alt text](image-28.png)
![alt text](image-29.png)
![alt text](image-19.png)
![alt text](image-31.png)



