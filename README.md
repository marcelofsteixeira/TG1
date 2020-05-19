# TG1 - 5º semestre de BD

 

Professor da Disciplina: Giuliano Bertoti 

 

# TG

 

Aluno: Marcelo Fernando de Souza Teixeira - RA1460281813028 

Orientador: Giuliano Bertoti 

Título do TG: Sistema para Auxílio na Alfabetização baseado em Machine Learning


# 1ª Quinzena de maio

Escolas brasileiras apresentam um grande volume de alunos por sala, e professores frequentemente sofrem dificuldades para acompanhar a progressão de cada aluno e ensinar todos com eficiência, problema que afeta em especial fases cruciais do Ensino Fundamental como a da alfabetização. Segundo dados de 2018 (INEP, 2018), a média de alunos por sala de ensino fundamental no Brasil é de 20 do primeiro ao terceiro ano (principal fase da alfabetização). O grande número de alunos por sala é agravado no ensino público (ZANLORENSSI & ALMEIDA, 2018), sendo a média próxima de 21 alunos em escolas do sistema municipal e estadual em comparação com escolas privadas, onde a média nesses anos é próxima de 16 por sala. Segundo relato de uma educadora no ano de 2018 (MANSANI, 2018), o número ideal de alunos por sala em anos de alfabetização seria de 15, número significativamente abaixo da média no ensino público.  
/
/
Em salas numerosas, é especialmente difícil manter a atenção de toda uma turma durante uma aula e acompanhar todos os alunos em todos os momentos, dando apoio para aqueles que passam pelas maiores dificuldades no processo de aprendizado. Um estudo de 2015 (GUILHERME, 2015) revelou que 20% do tempo das aulas no Brasil é perdido devido à desordem causada por alunos problemáticos que afetam a qualidade do ensino de toda a sala. No caso da alfabetização, problemas de aprendizagem causam enormes consequências para o desenvolvimento do aluno, uma vez que problemas na leitura e escrita tendem a causar grandes dificuldades nas fases seguintes do ensino. A Avaliação Nacional de Alfabetização do ano de 2016 (FARJADO, 2017) revelou que mais de 50% dos alunos de 8 anos de idade apresentavam, entre outros problemas de aprendizado, problemas de leitura.  
/
/
Somada a essa dificuldade, os alunos atualmente demonstram cada vez menos interesse no conteúdo do ensino formal do que conteúdos digitais, amplamente disseminados no dia-a-dia das famílias. Dados do Cetic (Centro Regional de Estudos para o Desenvolvimento da Sociedade da Informação) de 2018 (CETIC, 2018) revelaram que 77% de crianças entre 9 e 10 anos já são usuárias da internet. Uma vez que já é grande foco de atenção por parte das crianças, a tecnologia tem o potencial de causar um grande impacto positivo no aprendizado dos alunos, trazendo-os mais interesse na vida escolar e nos conteúdos apresentados. Um estudo do Reino Unido (PICTON, 2019) de 2018 revelou que para 86% de educadores o uso de tecnologia na fase de alfabetização aumentou o engajamento de alunos em sala.
/
/
Como forma de atenuar as dificuldades para a alfabetização nas escolas brasileiras, este trabalho se propõe a desenvolver um sistema para auxílio a professores e alunos que utilizará, entre outros recursos, a tecnologia de Machine Learning (aprendizado de máquina). O sistema proposto terá 2 componentes principais. O primeiro dos componentes será um aplicativo do aluno (AA), cuja função principal será mostrar em uma tela vídeos com instruções (WETZEL, 1994) a respeito da escrita de determinadas letras e, ao lado dos vídeos, quadros em branco onde o aluno poderá escrever a letra ensinada. O segundo componente será o aplicativo do professor (AP), que será responsável por cadastrar novas turmas, receber informações em tempo real (FINKELSTEIN, 2006) a respeito do desempenho dos alunos e guardar as informações reunidas de cada aula para que os professores possam, por exemplo, dedicar maior atenção para alunos com dificuldades na escrita das letras.
/
/
1.1. Objetivos do Trabalho  
O objetivo geral deste trabalho é o desenvolvimento de um sistema para auxílio a alunos e professores em turmas na fase da alfabetização, utilizando a tecnologia de machine learning para detectar os traços dos alunos e enviar avisos para os professores no caso dos que tiverem maiores dificuldades. 
/
/
1.2. Conteúdo do Trabalho 
O presente trabalho está estruturado em seis Capítulos, cujo conteúdo é sucintamente apresentado a seguir: 
No Capítulo 2 é feita a fundamentação das tecnologias que serão utilizadas no projeto, em especial o sistema de machine learning para a detecção dos traços dos alunos e o sistema de chamadas REST para o envio de avisos aos professores./
O Capítulo 3 apresenta o desenvolvimento da solução, contendo a descrição dos componentes do AA e do AP e como é realizada a sua integração./
No Capítulo 4 são apresentados os resultados de testes da aplicação desenvolvida neste trabalho, realizados com professores e alunos em fase de alfabetização./
O Capítulo 5 apresenta as considerações finais deste trabalho a partir da análise dos resultados obtidos com os testes em salas de aula./ 
