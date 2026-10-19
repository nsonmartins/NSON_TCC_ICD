Trabalho de Conclusão de Disciplina

Instituição: FAT - Faculdade de Tecnologia UERJ - Resende
Curso: Pós-graduação - Especialização em Engenharia Industrial
Disciplina: Introdução à Ciência de Dados (ICD)
Professor: Vahid Nikoofard
Aluno: Neilson Martins de Oliveira
Data: 20 de outubro de 2026

Predição de Cargas de Aquecimento e Resfriamento
 de Edificações Residenciais utilizando Machine Learning

Arquivo do projeto: “Building_Energy_Efficiency.ipynb” desenvolvido no VS Code, rodando com Python miniconda 3.14.7.
Base de dados: “ENB2012_data.xlsx” que pode ser baixada no link: https://archive.ics.uci.edu/static/public/242/energy+efficiency.zip

A pasta do meu repositório possui a seguinte estrutura:
NSON_TCC_ICD/
│
├── Building_Energy_Efficiency.ipynb
│
├── Dados/
│   └── energy+efficiency/
│       └── ENB2012_data.xlsx
│
└── README.md


Objetivo:
	Avaliar se é possível fazer predições das cargas de energia necessárias o aquecimento e o resfriamento de edificações residenciais com base em informações da arquitetura da edificação residencial.
Abordagem utilizada:
	Aprendizado supervisionado utilizando algoritmos de regressão (Regressão linear Múltipla e Random Forest Regressor). 
	Como temos duas variáveis de saída (Carga de Aquecimento e Carga de Resfriamento), foram criados dois modelos preditivos para cada variável. Ou seja, para a Carga de Aquecimento foram criados os modelos de Regressão Linear Múltipla e o modelo Random Forest Regressor. Do mesmo modo foi feito para a Carga de Resfriamento.  
Resumo dos resultados:
	Reunindo os resultados dos quatro modelos e comparando seus desempenhos, a regressão linear apresentou resultados satisfatórios. Mas o modelo Random Forest Regressor obteve desempenho superior para as duas variáveis alvos (Cargas energéticas).
	Na validação cruzada, para a Carga de Aquecimento, o Random Forest alcançou R2 médio de 0,9971. Para a Carga de Resfriamento o R2 médio foi de 0,9645. Além disso, apresentou menores valores de MAE e RMSE, confirmando a redução dos erros de previsão. Entretanto, o desempenho não foi igual para as duas cargas. O modelo de Aquecimento apresentou maior precisão, enquanto o de resfriamento apresentou erros mais elevados. Para compreender melhor esses erros, analisei os resíduos, que apresentaram que apresentaram as diferenças entre os valores observados e os valores previstos. Os gráficos mostram que os resíduos do modelo de Carga de Aquecimento estão mais concentrados próximos de zero. Para a Carga de Resfriamento, existe uma dispersão maior e alguns erros individuais mais expressivos.
	Também investiguei a importância das características arquitetônicas a técnica de importância por permutação. A Compacidade Relativa apresentou a maior importância preditiva nos dois modelos Random Forest. Esse resultado é interessante porque na análise exploratória, a Altura Total e a Área de Telhado apresentaram as correlações lineares mais expressivas com as cargas energéticas. Isto mostra que a correlação linear de uma variável não é a mesma coisa que sua importância para o desempenho de um modelo preditivo. A importância por permutação também não deve ser interpretada como uma relação de causalidade.

Conclusão:
 	Como conclusão, considero que o objetivo do projeto foi alcançado. Foi possível desenvolver um fluxo completo de Ciência de Dados, desde a inspeção e a análise exploratória até a construção, validação e comparação de modelos de Machine Learning. O Random Forest apresentou o melhor desempenho nas condições avaliadas, tanto para Aquecimento quanto para Resfriamento. Entretanto, algumas limitações precisam ser reconhecidas. A base de dados contém dados simulados, e os resultados não garantem que o mesmo desempenho seja obtido em edificações residenciais reais. Além disso, foram avaliados apenas dois algoritmos, sem uma otimização sistemática dos hiperparâmetros. 
	Como possibilidade de continuidade, seria interessante avaliar outros algoritmos, realiar ajustes de hiperparâmetros e utilizar dados de edificações reais. 
	Por fim, o principal resultado acadêmico deste trabalho foi a aplicação prática dos conhecimentos adquiridos na disciplina, especialmente na análise exploratória, na preparação dos dados, no treinamento e na avaliação de modelos preditivos.
