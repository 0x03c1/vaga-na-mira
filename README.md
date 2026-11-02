# Vaga na Mira: construa com IA o seu copiloto de carreira

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU_USUARIO/SEU_REPOSITORIO/blob/main/VagaNaMira.ipynb)

Material do minicurso que apresento no 9º Fórum de Administração e 5ª Jornada de Empreendedorismo e Trabalhabilidade.

Nesse minicurso vocês vão construir um copiloto de carreira com IA. Ele compara um currículo com uma vaga e aponta, requisito por requisito, o que o candidato atende, sempre mostrando o trecho do currículo que comprova. Ao longo da aula a gente compara esse copiloto com um filtro de palavras-chave parecido com os que muitas empresas usam, faz um teste de viés, protege os dados pessoais e gera um plano de estudos com cursos gratuitos. No fim, tudo vira um app com link, e vocês apresentam a ideia como se fosse uma startup.

Não precisa saber programar. O código está pronto e fica escondido no notebook. Quem programa pode abrir tudo e tem desafios extras.

## Para quem vai participar

1. Entrem na conta Google pessoal de vocês no navegador.
2. Gerem uma chave gratuita em https://aistudio.google.com/apikey (botão **Create API key**). Não compartilhem essa chave com ninguém.
3. Cliquem no botão **Abrir no Colab** lá em cima e depois em **Arquivo > Salvar uma cópia no Drive**. Se aparecer um aviso dizendo que o notebook não foi criado pelo Google, cliquem em **Executar mesmo assim**.
4. Sigam o notebook a partir do Passo 0.

O passo a passo completo, com o que deve aparecer em cada etapa e o que fazer se algo der errado, está em [docs/04_tutorial.md](docs/04_tutorial.md).

Se vocês estiverem num computador de laboratório, no final salvem o notebook, desconectem o Colab e saiam da conta Google.

## Para quem quiser replicar o minicurso

| Arquivo | O que tem |
|---|---|
| [docs/01_proposta.md](docs/01_proposta.md) | proposta completa: escolha do tema, justificativa, objetivos, ementa, conteúdo, cronograma e referências |
| [docs/02_plano_de_aula_e_roteiro.md](docs/02_plano_de_aula_e_roteiro.md) | plano de aula e roteiro minuto a minuto, pensado para professor remoto e turma em laboratório |
| [docs/03_material_teorico.md](docs/03_material_teorico.md) | roteiro dos slides com as minhas notas |
| [docs/04_tutorial.md](docs/04_tutorial.md) | tutorial para os alunos |
| [docs/05_desafio_e_avaliacao.md](docs/05_desafio_e_avaliacao.md) | desafio final, pitch e critérios de avaliação |
| [docs/06_guia_do_facilitador_e_laboratorio.md](docs/06_guia_do_facilitador_e_laboratorio.md) | checklist do laboratório, papel de quem acompanha a turma presencialmente, resultados de referência e problemas comuns |
| [VagaNaMira.ipynb](VagaNaMira.ipynb) | notebook usado na aula |
| [codigo/vaga_na_mira.py](codigo/vaga_na_mira.py) | o mesmo código em script, para rodar fora do Colab |
| [dados/](dados/) | vagas, currículos e gabarito, todos fictícios |

### Rodar no próprio computador

```bash
cd codigo
pip install -r requirements.txt
export GOOGLE_API_KEY="sua-chave"   # sem chave, roda em modo simulado
python vaga_na_mira.py              # placar de validação, teste de viés e um plano de exemplo
python vaga_na_mira.py --web        # também abre o app em http://127.0.0.1:7860
```

Tudo o que é usado é gratuito: Google Colab, API do Gemini (plano gratuito), google-genai, Pydantic, pandas e Gradio. As pessoas e empresas que aparecem nos dados são fictícias.
