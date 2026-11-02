# Proposta do minicurso

## Vaga na Mira: construa com IA o seu copiloto de carreira

**Texto para divulgação**

> O filtro do RH reprovaria você? Em três horas, você vai construir com inteligência artificial um copiloto que analisa currículos, comprova o que o candidato sabe, expõe as falhas dos filtros automáticos e monta um plano para conquistar a vaga. E vai sair com o protótipo de uma startup em mãos.

Outros títulos que considerei:

- Contratado pela IA: construa o copiloto que coloca você na frente da fila
- Do currículo à startup: IA para conquistar sua vaga e criar seu próprio negócio

| | |
|---|---|
| Evento | 9º Fórum de Administração e 5ª Jornada de Empreendedorismo e Trabalhabilidade |
| Público | estudantes da área de Informação e Comunicação, com vagas abertas a estudantes de Administração e cursos afins |
| Formato | eu conduzo a aula remotamente; a turma fica em laboratório, acompanhada por um facilitador presencial |
| Duração | 3 horas. Cerca de 20 minutos de teoria, 15 de demonstração e o restante em prática, desafio e apresentações |
| Organização | duplas por computador, revezando quem opera e quem acompanha o tutorial |
| Material | repositório público no GitHub com notebook, documentação, dados e código |
| Resultado | um copiloto de carreira funcionando, um app com link, um plano de carreira pessoal e um pitch de negócio |

## 1. Por que escolhi esse tema

O evento tem três eixos: administração, empreendedorismo e trabalhabilidade. Eu queria um minicurso de IA que conversasse com os três, que fosse acessível para quem não programa e que mesmo assim tivesse rigor, ou seja, que os alunos construíssem algo e verificassem se aquilo funciona, em vez de só conversar com um chatbot.

Comparei algumas opções usando cinco critérios com pesos diferentes:

- conexão com o evento (30%);
- curva de aprendizado baixa (25%);
- possibilidade de validar o resultado (20%);
- engajamento (15%);
- viabilidade com o formato remoto e laboratório (10%).

| Tema | Evento | Curva | Validação | Engajamento | Viabilidade | Nota |
|---|:-:|:-:|:-:|:-:|:-:|:-:|
| Agente de triagem de chamados de TI | 2 | 3 | 5 | 3 | 4 | 3,20 |
| App gerado por IA (Bolt, Lovable) | 3 | 4 | 2 | 5 | 2 | 3,25 |
| Automação no-code para pequenos negócios (n8n, Make) | 4 | 3 | 2 | 3 | 2 | 3,00 |
| Validação de ideia de startup com IA | 5 | 4 | 2 | 4 | 4 | 3,90 |
| Engenharia de prompt para produtividade | 3 | 5 | 2 | 3 | 5 | 3,50 |
| **Copiloto de carreira com IA** | **5** | **4** | **5** | **5** | **4** | **4,65** |

O copiloto de carreira ganhou com folga por alguns motivos:

- A dor é dos próprios alunos. Todo mundo ali vai procurar estágio ou emprego, e cada um sai da aula com um plano para uma vaga real que deseja.
- O que eles constroem é, na prática, o protótipo de uma startup de RH. O mesmo motor serve para comparar uma proposta de startup com um edital de inovação ou uma proposta de fornecedor com uma licitação, e esse pivô entra no desafio final.
- Dá para medir. Existe um gabarito feito por uma recrutadora, um filtro de palavras-chave para servir de comparação e uma verificação automática de que a IA não está inventando informações.
- Permite discutir viés e LGPD com um exemplo concreto, e isso interessa tanto a quem é de TI quanto a quem é de gestão.
- A curva é baixa. No Colab, o código fica escondido em células de formulário e o aluno só executa e escolhe opções em menus.

Também tem um caso que prende a atenção logo no começo. A Juliana, candidata fictícia ideal para a vaga de análise de dados, é reprovada pelo filtro de palavras-chave porque escreveu "planilhas" em vez de "Excel" e "consultas com SELECT" em vez de "SQL". A IA aprova a Juliana e mostra de onde tirou cada conclusão. Todo mundo entende o problema na hora, e a lição serve para o currículo de cada um.

As outras opções ficaram de fora por motivos práticos. A triagem de chamados é tecnicamente boa, mas fica longe do tema do evento. As ferramentas que geram apps a partir de texto têm poucos créditos gratuitos e o resultado é difícil de validar. As plataformas no-code exigem contas com limite de execução e ensinam mais a ferramenta do que o conceito. A validação de ideia de startup é envolvente, mas não tem como medir se a IA acertou, então aproveitei a ideia como pivô dentro do desafio.

## 2. Justificativa

A IA generativa mexeu nos dois lados da contratação. As empresas passaram a esperar que profissionais de tecnologia saibam integrar modelos de linguagem a sistemas com qualidade e responsabilidade, e o relatório *Future of Jobs 2025* do Fórum Econômico Mundial coloca IA e dados entre as habilidades que mais crescem. Ao mesmo tempo, o próprio recrutamento ficou automatizado: muitos currículos passam primeiro por filtros de palavras-chave ou por sistemas de IA. A regulação europeia (Regulamento (UE) 2024/1689, Anexo III) classifica esses sistemas como de alto risco, e há casos conhecidos de discriminação, como a ferramenta de recrutamento que a Amazon abandonou depois de perceber que ela penalizava currículos de mulheres (Dastin, Reuters, 2018).

No minicurso, os alunos constroem um sistema de IA aplicado ao recrutamento, medem a qualidade dele, testam viés e protegem dados pessoais de acordo com a LGPD. Pelo caminho, aprendem a escrever um currículo que funcione melhor para pessoas e para máquinas e montam um plano para desenvolver o que falta para a vaga que querem. Por fim, enxergam no que construíram uma oportunidade de negócio, com custo por análise e modelo de receita. Isso cobre a parte técnica, a trabalhabilidade e o empreendedorismo no mesmo projeto.

## 3. Público-alvo

O público principal são estudantes da área de Informação e Comunicação, de qualquer período. Estudantes de Administração e de cursos de gestão também conseguem acompanhar, e eu recomendo formar duplas misturando as áreas.

Há dois níveis dentro do mesmo notebook. Quem não programa executa as células, escolhe opções nos menus, edita textos e interpreta os resultados. Quem programa pode abrir o código e fazer desafios extras, como alterar a verificação de provas, criar novas variantes do teste de viés ou rodar o projeto localmente.

## 4. Objetivos

### Objetivo geral

Levar os participantes a construir, validar e apresentar uma solução de IA aplicada à empregabilidade, entendendo como ela funciona, quais riscos éticos e legais envolve e que potencial tem como negócio, e usar essa solução para planejar a própria carreira.

### Objetivos específicos

Ao final, espero que o participante consiga:

1. explicar de forma simples como um modelo de linguagem funciona e por que ele pode inventar informações;
2. usar uma IA por meio de API dentro de um programa;
3. ler e modificar um prompt com regras e uma saída estruturada;
4. comparar a solução com IA e um filtro de palavras-chave usando métricas;
5. verificar se o que a IA afirma tem comprovação no documento original;
6. fazer um teste de viés e aplicar anonimização de currículo, de acordo com a LGPD;
7. explicar o que é um agente que usa ferramentas e por que isso reduz invenções;
8. montar um plano de desenvolvimento pessoal para uma vaga real;
9. adaptar a solução para outro mercado e defender a ideia num pitch com custo e modelo de receita.

## 5. Pré-requisitos

Para os participantes: conta Google pessoal e celular à mão, porque o Google costuma pedir confirmação de login em computador novo. Não é preciso saber programar.

Para o laboratório: computadores com navegador atualizado, internet liberada para os endereços listados no guia do laboratório, projetor e som. A checklist completa está em `docs/06_guia_do_facilitador_e_laboratorio.md`.

Para a equipe: eu conduzo remotamente e preciso de uma pessoa no laboratório (professor ou monitor) acompanhando a turma.

## 6. Ferramentas

Tudo é gratuito e roda no navegador.

| Ferramenta | Uso |
|---|---|
| GitHub | distribuição do material e botão para abrir o notebook no Colab |
| Google Colab | onde o notebook roda, sem instalar nada |
| Google AI Studio e API do Gemini | modelo de linguagem, plano gratuito, uma chave por dupla |
| google-genai, Pydantic, pandas | chamada à IA, formato da resposta e métricas |
| Gradio | app web com link público temporário |
| Videoconferência | transmissão da aula para o projetor do laboratório |
| Padlet, Mentimeter ou Google Forms | mural para checkpoints, enquetes e entregas, acessado por QR code |

Se a chave não funcionar ou a API ficar fora do ar, o notebook passa sozinho para um modo simulado e todas as células continuam funcionando.

## 7. Ementa

Inteligência artificial generativa e mercado de trabalho. Funcionamento básico de modelos de linguagem e o problema da alucinação. Uso de IA por API. Prompts com regras e respostas estruturadas. Verificação de evidências. Validação com gabarito, solução de referência e métricas. Recrutamento automatizado e suas limitações. Viés algorítmico, LGPD e regulação de IA de alto risco. Agentes e uso de ferramentas. Protótipo de aplicativo web. Pivô de produto, custo por análise e modelo de negócio. Plano de desenvolvimento de carreira.

## 8. Conteúdo programático

| Unidade | Conteúdo | Onde aparece |
|---|---|---|
| IA e trabalhabilidade | como a IA mudou as profissões de TI e o recrutamento; filtros automáticos (ATS) | teoria e passo 3 |
| Como a IA funciona | tokens, previsão do próximo texto, temperatura, alucinação | teoria e passo 1 |
| Do chat ao produto | API, instruções de sistema, resposta estruturada, provas | teoria e passo 4 |
| Validação | gabarito, comparação com o filtro, acurácia, lacunas encontradas, candidatos prejudicados, provas conferidas | passos 3 e 5 |
| Ética e LGPD | viés, teste de viés, currículo cego, minimização de dados, regulação | passo 6 |
| Agentes | uso de ferramentas e catálogo verificado de cursos | passo 7 |
| Produto e negócio | app web, pivô, custo por análise, canvas, pitch | passos 8 e 10 e desafio |
| Carreira | análise do próprio currículo com uma vaga real, plano de quatro semanas, LinkedIn | passo 9 |

## 9. Cronograma

| Horário | Min | Etapa | O que acontece |
|---|:-:|---|---|
| 0:00 | 10 | Abertura | apresentação, formação das duplas, enquete sobre as dificuldades para conseguir estágio |
| 0:10 | 20 | Contextualização | IA e mercado, filtros de RH, como a IA funciona, validação, viés e LGPD, agentes, RH como negócio |
| 0:30 | 15 | Demonstração | eu mostro o app funcionando, o caso da Juliana, o teste de viés e o plano de carreira |
| 0:45 | 10 | Passo 0 | abrir pelo GitHub, salvar cópia, configurar a chave |
| 0:55 | 15 | Passos 1 a 3 | primeira chamada à IA, candidatos e vagas, filtro de palavras-chave |
| 1:10 | 20 | Passos 4 e 5 | análise com IA e validação nos dez pares (checkpoint 1) |
| 1:30 | 10 | Intervalo | |
| 1:40 | 15 | Passo 6 | teste de viés e currículo cego (checkpoint 2) |
| 1:55 | 15 | Passos 7 e 8 | plano de carreira e app (checkpoint 3) |
| 2:10 | 25 | Desafio | missões A, B e C |
| 2:35 | 20 | Pitch | cinco ou seis equipes, três minutos cada |
| 2:55 | 5 | Encerramento | próximos passos, avaliação, logout |

## 10. Onde está cada material

| Material | Arquivo |
|---|---|
| Plano de aula e roteiro | `docs/02_plano_de_aula_e_roteiro.md` |
| Material teórico | `docs/03_material_teorico.md` |
| Tutorial prático | `docs/04_tutorial.md` |
| Código-fonte | `VagaNaMira.ipynb` e `codigo/vaga_na_mira.py` |
| Desafio, critérios e rubrica | `docs/05_desafio_e_avaliacao.md` |
| Guia do facilitador e do laboratório | `docs/06_guia_do_facilitador_e_laboratorio.md` |

## 11. O que cada participante leva

- O copiloto funcionando no próprio Google Drive, com o repositório disponível para refazer quando quiser.
- Um app com link para usar e mostrar.
- O placar comparando o filtro de palavras-chave e a IA.
- O resultado do teste de viés, antes e depois do currículo cego.
- Um plano de quatro semanas para uma vaga real, com cursos gratuitos, projeto de portfólio, perguntas de entrevista e sugestão de título para o LinkedIn.
- Um pitch de negócio baseado no que construiu.
- Duas regras práticas para o currículo: usar as palavras da vaga e mostrar como comprova cada uma.

## 12. Referências

### Livros, artigos e normas

- ANDERSON, L. W.; KRATHWOHL, D. R. *A Taxonomy for Learning, Teaching, and Assessing*. New York: Longman, 2001.
- BACICH, L.; MORAN, J. (org.). *Metodologias ativas para uma educação inovadora*. Porto Alegre: Penso, 2018.
- BRASIL. Lei nº 13.709, de 14 de agosto de 2018. Lei Geral de Proteção de Dados Pessoais (LGPD).
- BRASIL. Senado Federal. Projeto de Lei nº 2.338, de 2023. Dispõe sobre o uso da inteligência artificial. Aprovado no Senado em dezembro de 2024 (conferir a tramitação atual).
- DASTIN, J. Amazon scraps secret AI recruiting tool that showed bias against women. *Reuters*, 10 out. 2018.
- HUYEN, C. *AI Engineering: Building Applications with Foundation Models*. Sebastopol: O'Reilly, 2025.
- O'NEIL, C. *Algoritmos de destruição em massa*. Santo André: Rua do Sabão, 2020.
- OSTERWALDER, A.; PIGNEUR, Y. *Business Model Generation: inovação em modelos de negócios*. Rio de Janeiro: Alta Books, 2011.
- RIES, E. *A startup enxuta*. Rio de Janeiro: Sextante, 2019.
- RUSSELL, S.; NORVIG, P. *Inteligência Artificial: uma abordagem moderna*. 4. ed. Rio de Janeiro: GEN LTC, 2022.
- UNIÃO EUROPEIA. Regulamento (UE) 2024/1689 (Regulamento da Inteligência Artificial), Anexo III.
- YAO, S. et al. ReAct: Synergizing Reasoning and Acting in Language Models. *ICLR*, 2023.

### Documentação e materiais online

- Documentação da API Gemini: https://ai.google.dev/gemini-api/docs
- SDK google-genai para Python: https://googleapis.github.io/python-genai/
- Google Colab: https://colab.research.google.com
- Gradio: https://www.gradio.app/docs
- Pydantic: https://docs.pydantic.dev
- OWASP Top 10 for LLM Applications 2025: https://genai.owasp.org/
- Anthropic, *Building effective agents* (2024): https://www.anthropic.com/engineering/building-effective-agents
- World Economic Forum, *The Future of Jobs Report 2025*: https://www.weforum.org/publications/the-future-of-jobs-report-2025/
- Stack Overflow Developer Survey 2025: https://survey.stackoverflow.co/
- Plataformas usadas no catálogo de cursos gratuitos: Kaggle Learn, SQLBolt, Microsoft Learn, Fundação Bradesco (Escola Virtual), Curso em Vídeo, freeCodeCamp, MDN, react.dev, GitHub Skills, Spring Guides, documentação do Docker, Cisco Networking Academy, Linux Journey, Escola Virtual.Gov, Khan Academy e Sebrae.
