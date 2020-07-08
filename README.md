# TG1 - 5º semestre de BD

 

Professor da Disciplina: Giuliano Bertoti 

 

# TG

 

Aluno: Marcelo Fernando de Souza Teixeira - RA1460281813028 

Orientador: Giuliano Bertoti 

Título do TG: Sistema para Auxílio na Alfabetização baseado em Machine Learning


# 1ª Quinzena de maio
1. INTRODUÇÃO\
\
Escolas brasileiras apresentam um grande volume de alunos por sala, e professores frequentemente sofrem dificuldades para acompanhar a progressão de cada aluno e ensinar todos com eficiência, problema que afeta em especial fases cruciais do Ensino Fundamental como a da alfabetização. Segundo dados de 2018 (INEP, 2018), a média de alunos por sala de ensino fundamental no Brasil é de 20 do primeiro ao terceiro ano (principal fase da alfabetização). O grande número de alunos por sala é agravado no ensino público (ZANLORENSSI & ALMEIDA, 2018), sendo a média próxima de 21 alunos em escolas do sistema municipal e estadual em comparação com escolas privadas, onde a média nesses anos é próxima de 16 por sala. Segundo relato de uma educadora no ano de 2018 (MANSANI, 2018), o número ideal de alunos por sala em anos de alfabetização seria de 15, número significativamente abaixo da média no ensino público.  
\
\
Em salas numerosas, é especialmente difícil manter a atenção de toda uma turma durante uma aula e acompanhar todos os alunos em todos os momentos, dando apoio para aqueles que passam pelas maiores dificuldades no processo de aprendizado. Um estudo de 2015 (GUILHERME, 2015) revelou que 20% do tempo das aulas no Brasil é perdido devido à desordem causada por alunos problemáticos que afetam a qualidade do ensino de toda a sala. No caso da alfabetização, problemas de aprendizagem causam enormes consequências para o desenvolvimento do aluno, uma vez que problemas na leitura e escrita tendem a causar grandes dificuldades nas fases seguintes do ensino. A Avaliação Nacional de Alfabetização do ano de 2016 (FARJADO, 2017) revelou que mais de 50% dos alunos de 8 anos de idade apresentavam, entre outros problemas de aprendizado, problemas de leitura.  
\
\
Somada a essa dificuldade, os alunos atualmente demonstram cada vez menos interesse no conteúdo do ensino formal do que conteúdos digitais, amplamente disseminados no dia-a-dia das famílias. Dados do Cetic (Centro Regional de Estudos para o Desenvolvimento da Sociedade da Informação) de 2018 (CETIC, 2018) revelaram que 77% de crianças entre 9 e 10 anos já são usuárias da internet. Uma vez que já é grande foco de atenção por parte das crianças, a tecnologia tem o potencial de causar um grande impacto positivo no aprendizado dos alunos, trazendo-os mais interesse na vida escolar e nos conteúdos apresentados. Um estudo do Reino Unido (PICTON, 2019) de 2018 revelou que para 86% de educadores o uso de tecnologia na fase de alfabetização aumentou o engajamento de alunos em sala.
\
\
Como forma de atenuar as dificuldades para a alfabetização nas escolas brasileiras, este trabalho se propõe a desenvolver um sistema para auxílio a professores e alunos que utilizará, entre outros recursos, a tecnologia de Machine Learning (aprendizado de máquina). O sistema proposto terá 2 componentes principais. O primeiro dos componentes será um aplicativo do aluno (AA), cuja função principal será mostrar em uma tela vídeos com instruções (WETZEL, 1994) a respeito da escrita de determinadas letras e, ao lado dos vídeos, quadros em branco onde o aluno poderá escrever a letra ensinada. O segundo componente será o aplicativo do professor (AP), que será responsável por cadastrar novas turmas, receber informações em tempo real (FINKELSTEIN, 2006) a respeito do desempenho dos alunos e guardar as informações reunidas de cada aula para que os professores possam, por exemplo, dedicar maior atenção para alunos com dificuldades na escrita das letras.
\
\
1.1. Objetivos do Trabalho\
O objetivo geral deste trabalho é o desenvolvimento de um sistema para auxílio a alunos e professores em turmas na fase da alfabetização, utilizando a tecnologia de machine learning para detectar os traços dos alunos e enviar avisos para os professores no caso dos que tiverem maiores dificuldades. 
\
\
1.2. Conteúdo do Trabalho \
O presente trabalho está estruturado em seis Capítulos, cujo conteúdo é sucintamente apresentado a seguir:\
No Capítulo 2 é feita a fundamentação das tecnologias que serão utilizadas no projeto, em especial o sistema de machine learning para a detecção dos traços dos alunos e o sistema de chamadas REST para o envio de avisos aos professores.\
O Capítulo 3 apresenta o desenvolvimento da solução, contendo a descrição dos componentes do AA e do AP e como é realizada a sua integração.\
No Capítulo 4 são apresentados os resultados de testes da aplicação desenvolvida neste trabalho, realizados com professores e alunos em fase de alfabetização.\
O Capítulo 5 apresenta as considerações finais deste trabalho a partir da análise dos resultados obtidos com os testes em salas de aula.

# 2ª Quinzena de maio
2. FUNDAMENTAÇÃO TÉCNICA \
A aplicação desenvolvida neste trabalho utiliza das tecnologias de AI e Machine Learning para auxiliar no ensino de crianças na fase da alfabetização, automatizando processos que anteriormente seriam delegados para professores e auxiliares de sala. Com o desenvolvimento dessa aplicação, o processo de ensino da escrita se torna mais envolvente para o aluno e mais facilmente gerenciável para professores, principalmente no caso de turmas com grande número de alunos (caso comum para o sistema educacional brasileiro). \
Neste capítulo serão apresentados os temas que baseiam o desenvolvimento deste trabalho, divididos entre as seções 2.1, sobre dados da educação no Brasil e uso de tecnologia por crianãs, e 2.2, sobre desenvolvimentos recentes nas áreas de AI e Machine Learning e sua aplicação para educação. \
2.1. Sistema Educacional Brasileiro e Uso de Tecnologia por Crianças\
Dados de 2019 do Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira, INEP, indicam que cerca de 89% das crianças em fase de alfabetização no Brasil, que se conclui no terceiro ano do ensino fundamental, são aprovadas para o ano seguinte e portanto tiveram sucesso nessa etapa do ensino (INEP, 2019). O resultado insuficiente do restante desses alunos pode ser atribuído à característica do ensino fundamental brasileiro de possuir salas com grandes números de alunos. Dados do mesmo instituto, do ano de 2018 (INEP, 2018), revelam que a média de alunos por sala de ensino fundamental no Brasil é de 20 do primeiro ao terceiro ano (principal fase da alfabetização). O grande número de alunos por sala é agravado no ensino público (ZANLORENSSI & ALMEIDA, 2018), sendo a média próxima de 21 alunos em escolas do sistema municipal e estadual em comparação com escolas privadas, onde a média nesses anos é próxima de 16 por sala. A média de alunos por sala no ensino fundamental no Brasil se encontra entre os resultados de países como Reino Unido, com 18.2 alunos por sala (UK DEPARTMENT FOR EDUCATION, 2011) e Estados Unidos, com 21.6 alunos por sala (NCES, 2012). \
Um dos principais resultados negativos da concentração de grande número de alunos por sala é a desordem causada pela falta de foco direcionada para cada aluno. Estatísticas do Teaching and Learning International Survey (Pesquisa Internacional de Ensino e Aprendizado), realizado pela OCDE em 2018 (TALIS, 2018) revelaram que cerca de 20% do tempo das aulas no Brasil é perdido devido à desordem causada por alunos problemáticos que afetam a qualidade do ensino de toda a sala. No caso da alfabetização, problemas de aprendizagem causam enormes consequências para o desenvolvimento do aluno, uma vez que problemas na leitura e escrita tendem a causar grandes dificuldades nas fases seguintes do ensino. A Avaliação Nacional de Alfabetização do ano de 2016 (INEP, 2017) revelou que mais de 50% dos alunos de 8 anos de idade apresentavam problemas de leitura, entre outros problemas de aprendizado. \
Apesar dos desafios do sistema educacional, é notável que os alunos nessa fase de ensino já possuem proficiência com o uso da tecnologia, o que facilita a adoção de soluções de auxílio de ensino baseadas em softwares desenvolvidos para essa finalidade. Dados do Cetic (Centro Regional de Estudos para o Desenvolvimento da Sociedade da Informação) de 2018 (CETIC, 2018) revelaram que 77% de crianças entre 9 e 10 anos já são usuárias da internet. No mesmo estudo, também foi revelado que 70% de alunos em áreas urbanas no Brasil possuíam computadores ou tablets em suas casas. Os benefícios do uso de softwares de ensino especificamente para a fase de alfabetização foram indicados por um estudo desenvolvido no Reino Unido (PICTON, 2019), onde 86% de educadores responderam que o uso de tecnologia nesse aumentou o engajamento de alunos em sala. 

2.2. Machine Learning, AI e Aplicações para Educação \
A área de Inteligência Artificial (AI) compreende todo o desenvolvimento de softwares e hardwares dedicados a emular comportamentos complexos da cognição humana, como percepção, racionalização, aprendizado, comunicação e atuação em ambientes diversos (NILSSON, 2009). Nos últimos anos, um dos principais campos de desenvolvimento da AI foi o de Machine Learning (ML), área dedicada à criação de previsões com alto nível de precisão baseada em um volume dados fornecidos a um algoritmo de aprendizado (MOHRI, ROSTAMIZADEH, TALWALKAR, 2012). \
No campo de Machine Learning, desenvolvimentos que envolveram o uso de redes neurais, compostas por múltiplos nós de processamento que, juntos, compõem um algoritmo de previsão (YEGNANARAYANA, 2003) permitiu um grande aumento na precisão do reconhecimento de padrões complexos. O uso de deep learning já acontece em áreas como a da saúde (YAMASHITA, 2018), otimização de indústrias (ROVITHAKOS, CHRISTODOLOU, 2000) e reconhecimento de fala (JAITLY, 2012), permitindo a solução de problemas que anteriormente não seriam possíveis de serem delegados para máquinas. \
O campo de reconhecimento e classificação de imagens (CHEN, 2019), aplica redes neurais para dividir uma determinada imagem em diversos setores e padrões que são reconhecidos pela rede de nós e categorizados conforme um processo de aprendizado realizado com imagens inseridas a priori na rede. Este processo pode ser supervisionado (ou seja, com seus resultados avaliados por uma pessoa ou outra máquina) ou não supervisionado (com os resultados e classificações gerados pela própria rede neural), como é a denominação comumente utilizada na área de Machine Learning (ZHU, GOLDBERG, 2009). \
Atualmente, diversas bibliotecas de software auxiliam o desenvolvimento de aplicações que utilizam redes neurais, sendo uma das principais e de maior utilização em todo o mundo a biblioteca de código aberto (open source) TensorFlow (TENSORFLOW, 2020). A biblioteca oferece uma API facilmente utilizável para linguagens de programação como Python (PYTHON, 2020) e Javascript (JAVASCRIPT, 2020) enquanto oferece um sistema de execução dos modelos baseado na linguagem C++ (ELLIS & STROUSTRUP, 1990) o que garante maior performance quando comparado a outras linguagens. Especificamente para as aplicações de reconhecimento de imagens e processamento de linguagem natural, a biblioteca TensorFlow apresenta resultados com alto nível de precisão e escaláveis para diversos níveis de conjuntos de dados e tamanhos de aplicações (ABADI, 2016).\
Para fins educacionais, algoritmos de deep learning são atualmente usados em sua maioria para a condução de estudos de qualidade de ensino (CIOLACU, 2017) e para prevenção de evasão de alunos (LYKOURENTZOU, 2009), devido à sua capacidade de interpretação dos padrões complexos necessários para esses problemas, como previsão de comportamentos e de retenção de conteúdos pelos alunos. Em setores específicos como o da medicina (KOLACHALAMA, 2018), técnicas de machine learning foram ensinadas de forma experimental e utilizadas durante a formação de médicos para auxiliar na precisão de seus diagnósticos. Para o ensino de alunos em fase de alfabetização, o uso de deep learning e reconhecimento de imagens pode se unir a mídias audiovisuais de eficácia comprovada, como vídeos instrucionais (WETZEL, 1994), para aumentar a qualidade das aulas e manter a atenção dos alunos.

# 3ª Quinzena de maio
3. Desenvolvimento 

O sistema desenvolvido para esse trabalho une tecnologias como o reconhecimento de imagens pela biblioteca Tensor Flow, implementada pela ferramenta Teachable Machine, em uma interface de usuário desenvolvida com a linguagem Javascript e o sistema de reprodução de vídeos da plataforma Youtube. Neste capítulo será apresentado o desenvolvimento do projeto, dividido nas seções 3.1, dedicada à arquitetura da aplicação e a integração das tecnologias utilizadas, a seção 3.2, dedicada ao desenvolvimento da interface para o usuário e a seção 3.3, dedicada ao sistema de detecção de problemas dos alunos.  \
3.1. Arquitetura do Sistema \
A aplicação desenvolvida para esse trabalho é baseada na linguagem de programação Javascript e, portanto, pode ser hospedada em um servidor e acessada por dispositivos de diversos tipos, como celulares e tablets ou até computadores pessoais (computadores de mesa ou notebooks) com dispositivos de escrita para cumprir a sua função de ensino. \
Após o login na aplicação, o usuário escolhe a letra que irá aprender a escrever, e é levado para uma página onde encontrará um vídeo de ensino e um quadro em branco onde irá escrever a letra ensinada no vídeo. O vídeo, hospedado é então reproduzido até o ponto em que a letra já foi ensinada e o usuário recebe um aviso que deverá começar a escrever. O quadro em branco, desenvolvido com a biblioteca Canvas Api, captura a forma escrita pelo aluno e a envia como formato de imagem para um modelo de reconhecimento pré-treinado e hospedado na plataforma Google Teachable Machine, que executa o reconhecimento utilizando a biblioteca TensorFlow. \
Após o reconhecimento da forma escrita pelo aluno, se ela apresentar uma grande probabilidade de ser a forma prevista para a letra ensinada, o aluno recebe um aviso de sucesso sobre a sua escrita. Se a forma estiver incorreta, ou seja, diferente da forma de letra com a qual o algoritmo hospedado no Google Teachable Machine foi treinado, são enviados avisos para o aluno de que ele deve seguir a forma mostrada no vídeo. No caso do aluno ter problemas repetidos para escrever a forma esperada, o vídeo é reproduzido novamente com as instruções de como a letra deve ser escrita.  \
3.2. Interface de Usuário
A interface de usuário foi desenvolvida com foco na simplicidade e facilidade para uso, com o objetivo de facilitar para que professores e alunos com pouca instrução pudessem utilizar a aplicação sem dificuldades. A tela de login da aplicação apresenta um design simples, indicando o nome do aluno, turma e senha que deve ser inserida. \
A tela principal da aplicação apresenta somente um campo para a reprodução do vídeo e um campo para a escrita da letra ensinada, com poucas margens para inputs indevidos que prejudicariam a experiência do usuário. O controle do vídeo é feito inteiramente pela aplicação, como forma de evitar que ele seja reproduzido em trechos incorretos, ou que o usuário escolha outro vídeo para ser reproduzido. As mensagens de sucesso e de erro também são exibidas com clareza e em formas simples, para que sejam compreendidas pelos alunos não alfabetizados. O design da página de escrita de letras foi programado de forma responsiva, para que ela encaixasse bem em telas de diferentes formatos (como é previsto para o uso da aplicação em salas de aula com diferentes tipos de equipamentos).  


# REFERENCIAS
INEP.   2019. Resultados finais do Censo Escolar 2019. Disponível em http://portal.inep.gov.br/web/guest/resultados-e-resumos .Acessado em 29/06/2020  \
INEP. 2018. Brasil, regiões e Ufs, Disponível em http://portal.inep.gov.br/web/ guest/indicadores-educacionais Acessado em 29/06/2020  \
INEP. 2017. Relatório Saeb-Ana 2016 Panorama Do Brasil E Dos Estados. Disponível em 
http://portal.inep.gov.br/informacao-da-publicacao/-/asset_publisher/6JYIsGMAMkW1/document/id/1510096 . Acessado em 29/06/2020  \
UK DEPARTMENT OF EDUCATION. 2012 Class Size and education in England evidence report. Disponível em https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/183364/DFE-RR169.pdf  . Acessado em 29/06/2020  \
NCES. 2012. Schools and Staffing Survey (SASS). Disponível em https://nces.ed.gov/surveys/sass/tables/sass1112_2013314_t1s_007.asp . Acessado em 29/06/2020  \
Zanlorenssi, G & Almeida, R. “O número de Alunos nas Salas de Aula do Brasil”. Nexo Jornal, 19/02/2018. Disponível em https://www.nexojornal.com.br/grafico/2018/02/19/O-n%C3%BAmero-de-alunos-nas-salas-de-aula-do-Brasil Acessado em 29/06/2020  \
TALIS. 2018. SPSS 2018 international. Disponível em http://www.oecd.org/education/talis/talis-2018-data.htm  . Acessado em 29/06/2020  \
Cetic. Tic Kids Online Brasil 2018 Principais Resultados, Disponível em https://www.cetic.br/media/analises/tic_kids_online_brasil_2018_coletiva_de_imprensa.pdf Acessado em 29/06/2020  \
Picton, I. “Teachers’ use of technology to support literacy in 2018”. Literacy Trust, 04/2019. Disponível em https://literacytrust.org.uk/documents/2371/ Teachers_Use_of_Technology_report.pdf Acessado em 29/06/2020  \
WETZEL, CD. et al. Instructional Effectivenes of video media. APA PsycNet, 1994.
INTRO. Javascript. INFO, disponível em https://javascript.info/intro Acessado em 29/06/2020  \
Google Creative Lab. Interplay Mode, Disponível em https://experiments. withgoogle.com/interplay-mode Acessado em 29/06/2020  \
NILSSON, N. Artificial Intelligence: A New Synthesis. Morgan Kauffman, 2009.  \
MOHRI, M. et al. Foundations of Machine Leaning. MIT Press, 2012   \
YEGNANARAYANA, B. Artificial Neural Networks. PHI, 2004.  \
YAMASHITA, R. et al. Convolutional neural networks: an overview and application in radiology.Insights into Imaging 9, 2018.  \
ROVITHAKIS, G & CHRISTODOULOU, M. Adaptive Control with Recurrent High-order Neural Networks. Springer-Verlag London, 2020.  \
JAITLY, N. et al  Application Of Pretrained Deep Neural Networks To Large Vocabulary Speech Recognition. Disponível em https://research.google/pubs/pub38130/ . Acessado em 29/06/2020  \
CHEN, C. et al This Looks Like That: Deep Learning for
Interpretable Image Recognition. Disponível em  http://papers.nips.cc/paper/9095-this-looks-like-that-deep-learning-for-interpretable-image-recognition.pdf . Acessado em 29/06/2020  \
ZHU, X. & GOLDBERG, A.  Introduction to Semi-Supervised Learning Disponível em https://www.morganclaypool.com/doi/abs/10.2200/S00196ED1V01Y200906AIM006 . Acessado em 29/06/2020  \
ABADI, M. et al. TensorFlow: A System for Large-Scale Machine Learning. Disponível em https://www.usenix.org/system/files/conference/osdi16/osdi16-abadi.pdf. Acessado em 29/06/2020  \
PYTHON. About. Disponível em https://www.python.org/about/ . Acessado em 29/06/2020  \
JAVASCRIPT. Intro https://javascript.info/intro . Acessado em 29/06/2020  \
TENSORFLOW. About. Disponível em https://www.tensorflow.org/about . Acessado em 29/06/2020  \
ELLIS, M. & STROUSTRUP, B. The Annotated C++ Reference
Manual. Disponível em https://cds.cern.ch/record/212867/files/0201514591_TOC.pdf . Acessado em 29/06/2020.  \
CIOLACU M. et al. Education 4.0 — Fostering student's performance with machine learning methods. Disponível em https://ieeexplore.ieee.org/abstract/document/8259941 . Acessado em 29/06/2020  \
LYKOYRENTZOU, I. et al.   Dropout prediction in e-learning courses through the combination of machine learning techniques. Disponível em https://www.sciencedirect.com/science/article/abs/pii/S0360131509001249 . Acessado em 29/06/2020.  \
KOLACHALAMA, V. Machine learning and medical education. Disponível em https://www.nature.com/articles/s41746-018-0061-1/ . Acessado em 29/06/2020.
