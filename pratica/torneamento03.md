<h1>SIMULAÇÕES DE PROCESSOS DE TORNEAMENTO</h1>

## Peça 3
<img width="600" alt="image" src="https://github.com/user-attachments/assets/ef3d712f-43ae-48dc-97be-31fa10471873" />

### Configuração
Selecionando a opção Manufatura, que é o espaço de trabalho de fabricação, simula as ferramentas de fabricação de um torno, e seus percursos. Na aba Torneamento, e Configurações, criamos uma Nova Configuração. Esta opção dará início à configuração do processo de fabricação. 
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/3be4cabf-6bbe-47dd-9251-96e4b2e1408f" />
<p>
Uma janela de configuração será aberta, onde teremos três abas. A primeira aba (Configuração), selecionamos o Tipo de operação como "Torneamento ou Fresagem". Em Sistemas de coordenadas de trabalho (WCS), mudamos a Orientação como "Plano/eixo z e eixo Y". Habilitamos "Inverter eixo Z", e "Inverter eixo Y". O eixo Z será a referência de comprimento, e o eixo X o diâmetro da peça.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/18845a8b-404d-47ee-85a8-5aac41eeaccb" />
<p>
Na aba Bloco, o Modo será um "Cilíndro de tamanho fixo", Posição do modelo como "Deslocamento da frente", com 60mm de Diâmetro de bloco, 122mm de Comprimento e 2mm de Deslocamento. Note que as Dimensões do modela já são exibidas como referência.  
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/b4cd33ce-5bd2-4e29-8a02-810a26da9523" />

### Facejar
  
A primeira etapa do processo será Facejar a peça. Selecionamos na aba Torneamento, o primeiro ícone. Ou expandir a aba, e selecionar "Facejar". Uma janela será aberta chamada Face contendo cinco abas: Ferramenta, Geometria, Raio, Passos e Vincular.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/9fda857f-3995-43c8-bdb8-d7a50b92ad70" />
<p>
Na primeira aba, Ferramenta, devemos selecionar qual ferramenta fará o Facejamento da peça.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/1bd6599c-9cbf-4747-a327-ba2161d4d983" />
<p>
Optaremos na Biblioteca do Fusion, Ferramentas de torneamento (métrico). Escolheremos a ferramenta CNMT09T308-DCLN-R (CNMT Right Hand).
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/1d7237fe-0cf0-4ae7-a23b-05170dae7cc1" />
<p>
A ferramenta já é vista na visão frontal, posicionada no lado direito da peça, aguardando o término da configuração, e execução da simulação. Nas demais opções mantemos as configurações como padrão.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/2bd7f753-4b8c-4cb8-8e3d-cd0180a2f2fb" />
<p>
Em Navegador (lado esquerdo), clicamos com o botão direito em [T1] Face, e escolhemos "Simular". Esta etapa dará início ao processo de simulação de Facejamento, onde a face frontal será facejada pela ferramenta. Clicando na seta de animação para direita, a ferramenta se moverá, deixando uma área verde, indicando que a superfície foi trabalhada.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/7c6d03a4-fa9a-44fc-85a4-a0d6cdccad46" />

### Desbaste de Perfil 1
Faremos o desbaste no primeiro segmento da peça, utilizando em Torneamento, a opção "Desbaste do perfil de torneamento". Será aberta uma janela, semelhante aos recursos de Facejamento, chamada "Desbaste de Perfil". Na aba Ferramentas, manteremos as mesmas configurações utilizadas anteriormente.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/9130123e-9ecf-4053-b2f4-4aae3dab6a0e" />
<img width="600" alt="image" src="https://github.com/user-attachments/assets/9509cdf1-c072-4f05-980e-96488e3f3b03" />
<p>
Na aba Geometria, iremos ajustar os limites que a ferramenta percorrerá ao longo do segmento a ser desbastado. Para isso, arrastamos a linha "Voltar" até o extremo do segmento desejado. Finalizamos com Ok.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/9e2f9580-fb88-4661-91c5-c7880c4b36df" />
<p>
Clicando com o botão direito em Configuração1, em Navegação, escolhemos "Simular". Note que a partir de um cilíndro cinza, ao final da simulação aparecerá uma face verde, que foi facejada, e uma área azul, por onde a ferramenta realizou o desbaste. 
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/f622bafc-34f2-42c0-bab0-e4046ed2ac84" />
<img width="600" alt="image" src="https://github.com/user-attachments/assets/76698be4-dc25-43f5-81c7-95011ee8e89a" />


### Desbaste de Perfil 2

Para realizar outro desbaste no último segmento da peça, repetimos os passos anteriores. Na aba Geometrial, o deslocamento frontal será ajustado no extremo inicial do segmento da peça que não foi concluído.
<p>
<img width="600" alt="image" src="https://github.com/user-attachments/assets/6b036acc-85d8-401e-bda1-48fd2ad86752" />
<p>

### Acabamento de Perfil 1



### Acabamento de Perfil 2

