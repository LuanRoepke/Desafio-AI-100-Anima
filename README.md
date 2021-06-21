# Desafio-AI-100-Anima: LUAN ALYSSON ROEPKE (realizado sozinho)
Descrever como foi executado o desafio 1 do curso engenheiros de IA by Microsoft


# Primeira etapa CONJUNTOS DE DADOS

Nessa etapa após baixar os dados para o computador local, precisa-se enviar para a nuvem no Azure Machine Learning no caminho conjunto de dados;


# Segunda etapa Explorar Dados

Diante da quantidade de colunas precisamos filtrar aquilo que realmente o cliente espera, prever notas de ciencias naturais em relação a matemática NU_NOTA_CN como Label e NU_NOTA_MT como feature;

Também podemos eliminar linhas sem informações da NU_NOTA_MT, e normalizar como opção, acabei fazendo, mas não era necessário já que o valor são de mesma escala;
Em seguida pode ser executado para verificar alguma incompatibilidade, se estiver tudo certo, pode dar sequencia para os próximos passos;


# Terceira etapa Pipeline de treinamento

Nessa etapa, vamos fazer um treinamento dos dados, para depois conseguir prever novos valores inseridos,

Para isso usamos as seguintes ferramentas:

 SPLIT DATA: vai dividir em 70% para treinar modelo e 30% para pontuar a precisão do teste
 
 LINEAR REGRESSION: algorítimo de machine learning para prever valores futuros em relação ao que se tem nos dados
 
 TRAIN MODEL: irá treinar os 70% dos dados usando o algorítimo acima.
 
 SCORE MODEL: irá pontuar valores em relação aos 30% que foi usado para fazer comparativo entre o certo e o previsto.
 
 EVALUETE MODEL: irá concluir através de métricas se o treinamento foi eficaz


# Quarta etapa Pipeline de inferência

Para inferir (prever) valores, precisa alterar algumas pipelines do treinamento

Tirar dados do enem e inserir agora manualmente (ENTER DATA MANUALLY) + ENTRADA PELA WEB
Excluir avaliação de modelo e inserir (EXECUTE PHYTON SCRIPT)

Abaixo 9 valores previstos pela Machine learning:

|NU_NOTA_CN PREVISTA       |       NU_NOTA_MT ENVIADO MANUALMENTE|
|--------------------------|-------------------------------------|
|     388.685959           |                    326              |
|     537.011854           |                    654              |
|     623.384555           |                    845              |
|     683.528896           |                    978              |
|     483.650709           |                    536              |
|     297.791128           |                    125              |
|     457.422349           |                    478              |
|     670.866929           |                    950              |
|     361.100961           |                    265              |
     

   Dessa forma se conclui que quem é bom em matemática, teve mais dificuldade em CN, porém a precisão do treino não ficou muito precisa e talvez deveria usar outro algoritimo para verificar se tem melhor validação.
