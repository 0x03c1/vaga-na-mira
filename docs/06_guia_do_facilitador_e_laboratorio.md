# Guia do facilitador e do laboratório

Escrevi este guia para três pessoas: para mim, que vou conduzir a aula remotamente; para quem vai acompanhar a turma no laboratório; e para a equipe de TI que prepara a sala.

## 1. Preparação do laboratório (TI, até três dias antes)

### Endereços que precisam estar liberados (HTTPS, porta 443)

| Endereço | Para quê |
|---|---|
| `github.com`, `raw.githubusercontent.com` | repositório do minicurso |
| `colab.research.google.com`, `*.colab.googleusercontent.com`, `*.googleusercontent.com` | Google Colab |
| `accounts.google.com`, `drive.google.com` | login e cópia do notebook |
| `aistudio.google.com` | geração da chave de API |
| `generativelanguage.googleapis.com` | API do Gemini, chamada pelo Colab |
| `pypi.org`, `files.pythonhosted.org` | instalação de pacotes dentro do Colab |
| `*.gradio.live` | link público do app (opcional) |
| `padlet.com`, `mentimeter.com` ou `forms.gle` | mural e enquetes, conforme a ferramenta escolhida |

### Computadores

- [ ] Chrome, Edge ou Firefox atualizado, com pop-ups e cookies de terceiros permitidos para os domínios do Google.
- [ ] Teste completo em um computador com uma conta Google: README, Abrir no Colab, passo 0 até o passo 8.
- [ ] Data e hora do sistema corretas, porque o login do Google falha quando o relógio está errado.
- [ ] Nenhuma extensão bloqueando scripts no navegador.

### Sala

- [ ] Projetor e caixa de som ligados ao computador do facilitador.
- [ ] Videoconferência testada comigo, com áudio nos dois sentidos e a câmera mostrando a turma.
- [ ] Um microfone para as perguntas da turma (pode ser o do próprio notebook).
- [ ] QR code do mural impresso ou no slide.

Quando muita gente faz login no Google a partir da mesma rede, é comum aparecer a tela de "confirme que é você". Por isso peço que todos levem o celular.

## 2. Minha preparação

### Uma semana antes

- [ ] Publicar o repositório e trocar `SEU_USUARIO/SEU_REPOSITORIO` pelo endereço real no README e no tutorial.
- [ ] Executar o notebook inteiro com uma chave de verdade e anotar os resultados na seção 3.
- [ ] Conferir os limites do plano gratuito (https://ai.google.dev/gemini-api/docs/rate-limits) e os preços (https://ai.google.dev/gemini-api/docs/pricing), e ajustar `PAUSA_MINIMA` e os valores do passo 10 se precisar.
- [ ] Abrir cada link do catálogo de cursos (`CATALOGO`, na célula 0.2) e confirmar que continua no ar e gratuito. Se a instituição tiver cursos próprios, vale incluir.
- [ ] Montar os slides a partir de `03_material_teorico.md`.
- [ ] Criar o mural, com colunas para o passo 0, os três checkpoints, os links, a missão A e o pitch, e o formulário de avaliação.

### Dois dias antes

- [ ] Mandar o e-mail para os participantes (seção 6) e a lista da seção 1 para a TI.
- [ ] Conversar uns 20 minutos com o facilitador sobre o roteiro, as contingências e a seção 4.

### Uma hora antes

- [ ] Deixar o meu notebook já executado, com as saídas visíveis, e o app aberto. É o meu plano B para a demonstração.
- [ ] Testar áudio e vídeo com o laboratório.
- [ ] Deixar o zoom do navegador entre 125% e 150% para compartilhar a tela.

## 3. Resultados de referência

### Filtro de palavras-chave

O resultado é sempre o mesmo, porque o filtro não usa IA:

| Acurácia | Lacunas encontradas | Candidatos subestimados |
|:-:|:-:|:-:|
| 0,70 | 0,93 | 2 (Juliana na vaga de dados e Carlos na de segurança) |

Os três erros do filtro:

| Par | Filtro | Gabarito | Motivo |
|---|---|---|---|
| Ana na vaga web | alta | média | o "quero aprender React" |
| Juliana na vaga de dados | baixa | alta | sinônimos |
| Carlos na vaga de segurança | média | alta | o curso em inglês, "Cybersecurity" |

### Com IA

Preencho depois do meu teste com chave real:

| Versão | Acurácia | Lacunas encontradas | Candidatos subestimados | Provas verificadas |
|---|:-:|:-:|:-:|:-:|
| IA com verificação de provas | | | | |
| Diferença no teste de viés sem proteção | | | | |

### O gabarito

A regra é: todos os obrigatórios atendidos é alta, metade ou mais é média, menos que isso é baixa.

| Par | Nível | Por quê |
|---|---|---|
| Ana, web | média | tem HTML/CSS, JavaScript e Git; React não, só a vontade de aprender |
| Ana, suporte | média | tem Windows e Office (monitoria) e atendimento; falta redes |
| Ana, dados | baixa | tem Excel; faltam SQL e Power BI |
| Carlos, suporte | alta | Windows e Office, redes e atendimento |
| Carlos, segurança | alta | redes, Linux e segurança (Introduction to Cybersecurity) |
| Carlos, back-end | baixa | não tem nenhum obrigatório |
| Juliana, dados | alta | Excel (tabelas dinâmicas e PROCV), SQL (SELECT e JOIN) e Power BI |
| Juliana, web | baixa | não tem nenhum obrigatório |
| Rafael, back-end | alta | tem todos |
| Rafael, dados | baixa | tem SQL; faltam Excel e Power BI |

### Discussões que costumam aparecer

- A IA às vezes separa "HTML e CSS" ou "Windows e pacote Office" em dois requisitos. Nesses casos o nível não muda, mas é um bom exemplo de por que o prompt pede para manter os requisitos agrupados como a vaga escreveu.
- O "Excel intermediário" da Ana atende "Excel (tabelas dinâmicas, PROCV)"? No gabarito eu considerei que sim, mas um avaliador mais rigoroso poderia discordar. Gabarito ambíguo existe no mundo real, e vale discutir isso com a turma.

## 4. Problemas comuns

| O que acontece | Causa provável | Solução |
|---|---|---|
| Aviso "Este notebook não foi criado pelo Google" | aviso padrão para notebooks vindos do GitHub | clicar em Executar mesmo assim |
| As alterações não salvam | estão no notebook original, não na cópia | Arquivo > Salvar uma cópia no Drive |
| "Erro: a API recusou a chave" | chave incompleta ou nome do secret errado | gerar a chave de novo, usar exatamente `GOOGLE_API_KEY` e ligar o acesso ao notebook |
| Aparece um campo pedindo a chave | o secret está sem acesso ao notebook | ligar o acesso e executar a 0.2 de novo |
| "A API pediu uma pausa (código 429)" | limite por minuto do plano gratuito | esperar; o código tenta de novo sozinho |
| O 429 não para ou a cota do dia acabou | muitas execuções com a mesma chave | gerar uma chave na conta da outra pessoa da dupla, ou seguir em modo simulado criando uma célula com `MODO_SIMULADO = True` |
| `NameError: ... is not defined` | célula pulada ou ambiente reiniciado | Ambiente de execução > Executar anteriores |
| Modelo não encontrado (404) | o nome do modelo mudou | o motor escolhe outro sozinho; se não escolher, criar uma célula com `MODELO = escolher_modelo("")` |
| O AI Studio não está disponível para a conta | conta institucional ou de menor de idade | usar uma conta pessoal de maior de idade, ou o modo simulado |
| O link gradio.live não aparece | a rede bloqueia esse tipo de conexão | usar o app dentro do notebook |
| O Colab desconectou | inatividade ou queda da rede | Ambiente de execução > Executar anteriores (a chave continua salva nos Secrets) |

## 5. O que o facilitador faz em cada momento

| Momento | O que fazer |
|---|---|
| Antes de começar | ligar projetor e som, entrar na chamada, testar comigo e deixar o QR code visível |
| Abertura | formar as duplas misturando quem programa com quem não programa, e TI com Administração |
| Passo 0 | circular pela sala; é o momento que mais trava. O objetivo é todo mundo com o motor ligado, mesmo que em modo simulado |
| Durante a aula | levar ao microfone as dúvidas que interessam à turma toda e resolver as individuais com a seção 4 |
| Desafio | juntar as duplas em equipes, cronometrar e avisar quando faltarem cinco minutos |
| Pitch | controlar os três minutos de cada equipe e passar o microfone |
| Final | conferir em cada computador se a pessoa saiu da conta Google |

## 6. E-mail para os participantes (dois dias antes)

**Assunto:** Minicurso Vaga na Mira: o que levar

> Olá, pessoal!
>
> No minicurso Vaga na Mira vocês vão construir, no laboratório, um copiloto de carreira com inteligência artificial. Ele analisa currículos, mostra o que comprova cada competência, testa se a IA trata todos os candidatos da mesma forma e monta um plano para a vaga que vocês querem. Não precisa saber programar.
>
> Levem:
> - o login e a senha da sua conta Google pessoal, e o celular para confirmar o acesso;
> - o texto de uma vaga real que vocês gostariam de conquistar (do LinkedIn ou de qualquer site de vagas);
> - se quiserem, o currículo em texto, sem CPF, telefone e endereço.
>
> Se quiserem adiantar, entrem em https://aistudio.google.com/apikey, aceitem os termos e criem a chave. Leva dois minutos.
>
> O material está em [LINK DO REPOSITÓRIO].
> Local: [LABORATÓRIO]. Data e horário: [DATA E HORA].
>
> Até lá!

## 7. Mensagens para o slide ou o chat

- **Abertura:** Repositório: [LINK]. Cliquem em Abrir no Colab e depois em Arquivo > Salvar uma cópia no Drive.
- **Passo 0:** Chave em https://aistudio.google.com/apikey. No Colab: ícone de chave, nome `GOOGLE_API_KEY`.
- **Checkpoint 1:** Filtro: acurácia __ e subestimados __. IA: acurácia __ e subestimados __.
- **Checkpoint 2:** Que outra informação do currículo pode revelar gênero, idade ou origem?
- **Checkpoint 3:** Postem o link gradio.live e testem o da dupla do lado.
- **Desafio:** Missão A com todos por 10 minutos. Depois, missão B ou C em equipe.
- **Final:** Salvem, desconectem o Colab e saiam da conta Google. Avaliação: [LINK].

## 8. Outros formatos

| Formato | Ajuste |
|---|---|
| 2 horas | 15 minutos de teoria e 10 de demonstração; sem o experimento de temperatura e sem o passo 10; desafio só com a missão A; pitch com três equipes |
| 4 horas | incluir leitura de currículo em PDF (upload no Colab e extração do texto) e um conjunto maior de vagas criado pela turma; desafio de 40 minutos |
| Turma toda remota | o mesmo roteiro, com checkpoints pelo chat e desafio em salas separadas |
| Sem acesso à API | modo simulado do começo ao fim; o foco vai para validação, viés e negócio, e o filtro continua mensurável |
