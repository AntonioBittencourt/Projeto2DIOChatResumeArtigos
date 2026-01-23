# Introdução
É proposto o seguinte desafio na plataforma DIO:
"Neste desafio, você desenvolverá um chat interativo que responderá com base no conteúdo dos seus arquivos PDF. Para isso, utilizaremos conceitos de IA generativa, embeddings e buscas vetorizadas para estruturar um sistema capaz de entender, processar e responder perguntas a partir de documentos específicos. Essa abordagem permitirá que você crie um modelo personalizado de assistência virtual focado em um conjunto de informações proprietárias, sem depender unicamente do conhecimento geral de modelos pré-treinados."
"Imagine que você é um estudante de Engenharia de Software, prestes a escrever seu Trabalho de Conclusão de Curso (TCC). Para isso, você precisa revisar e correlacionar diversos artigos científicos. Entretanto, à medida que acumula mais documentos, torna-se cada vez mais difícil extrair informações relevantes e conectar ideias entre diferentes textos."

"Diante desse desafio, você decide utilizar inteligência artificial para facilitar esse processo, criando um sistema de busca inteligente capaz de interpretar os PDFs, organizar informações e gerar respostas relevantes com base no conteúdo carregado."


# Implementação

Conforme sugerido, foi usada a plataforma AI Foundry da Azure. A implementação acabou sendo mais simples do que o exibido no tutorial da Azure, devido as melhorias implementadas nas últimas versões Nâo é mais necessário criar AI Hubs, AI Search ou gerenciar o arquivo vetorizado, apenas o projeto. A complexidade da implementação é mais escondida, simplificando o processo de criação. Primeiramente criamos os artigos fictícios que são usados para teste. Eles foram gerados pelo Copilot e estão presentes neste Github na pasta artigos. Depois entramos no Playground do AI Foundry, onde é feito o deploy dos modelos Gpt 5.1 Chat e EmbeddedVectors3-LArge(transforma de texto para vetor e vice-versa), e colocamos as instruções para fornescer um contexto. Estas instruções estão presentes na figura 1. Antes mesmo de anexar os arquivos testamos a capacidade do chat de fornescer respostas por meio de conhecimento adquirido por outras fontes. Perguntamos a ele sobre SNA(Social Network Analysis) e a definição de engenharia de software. Esta interação está presente na segunda figura.

![Instruçõaes do Foundry](imagens/Projeto2DIOInstrucoes.jpg)
![Primeiro Prompt de Inteação](imagens/Projeto2DIOtesteprompt.jpg)
![Primeiro Prompt de Inteação Parte 2](imagens/Projeto2DIOtesteprompt2melhorimagem.jpg)

A seguir é feita a anexação dos arquivos gerados por IA. Como presente na figura abaixo.

![Artigos Anexados](https://github.com/AntonioBittencourt/Projeto2DIOChatResumeArtigos/blob/main/inputs/imagens/Projeto2DIOArtigosAnexados.jpg)

Com a anexação dos arquivos é feita uma pergunta com base no conteúdo dos artigos.

![Resposta do Chat](imagens/Projeto2DIOresposta1semcitacao.jpg)

Em seguida mudamos as instruções para que as respostas apareçam em formato de citação.

![Resposta do Chat em formato de citação](imagens/Projeto2DIOresposta1comcitacao.jpg)

E é feita outra pergunta para um novo artigo.

![Resposta do Chat](imagens/Projeto2DIOresposta2.jpg)

Por último é feita a criação do agente de IA a partir do projeto implementado. Chamamos esse agente de ResumeArigos. Já em formato de agente fazemos um último teste perguntando sobre definições externas aos artigos e sobre os artigos anexados.

![Resposta do Agente - Conteúdo Externo](imagens/Projeto2DioAgente.jpg)
![Resposta do Agente - Conteúdo dos Artigos](imagens/Projeto2DioAgenteResposta3.jpg)


# Conclusão
Percebemos que o Azure AI Foundry faz um bom trabalho ao ser treinado em artigos e resumi-los. Agentes criados como esse podem ajudar um estudante a organizar e entender informações pertinentes ao seu TCC, além de poder ser usado em ambiente de trabalho resumindo regulamentos, relatórios ou qualquer outra fonte de informação em PDF. A implementação de agentes com AI Foundry foi bastante simplificada nas últimas versões, permitindo que a complexidade fique escondida, sendo acessível a usuários mais avançados e facilitando o uso por usuários iniciantes ou intermediários.

