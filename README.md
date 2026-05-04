# Interior+: Dados, algoritmos e caminhos para a revitalização do interior de Portugal 

Projecto de análise documental e textual sobre o interior de Portugal, com foco em três eixos complementares: abandono rural, desenvolvimento rural e programas de apoio ao interior.

O trabalho cruza recolha histórica no Arquivo.pt, limpeza e normalização de texto, classificação por temas e uma síntese visual interactiva em dashboard.

## Objectivo

O objectivo do projecto é compreender como o interior rural foi descrito ao longo do tempo, que factores surgem associados ao abandono, que instrumentos de políticas pública são referidos para o desenvolvimento rural e como essas narrativas evoluem entre fontes mediáticas e institucionais.

## O que inclui

- Recolha de dados históricos no Arquivo.pt, com cobertura temporal alargada, através de extração automática pela API.
- Limpeza, normalização e armazenamento dos dados extraídos em ficheiros CSV dedicados.
- Uma solução preliminar de extração de nomes de localizações a partir dos snippets, que pretendemos continuar a desenvolver.
- Classificação temática por palavras-chave e taxonomias interpretativas.
- Comparação entre discurso mediático e institucional.
- Dashboard HTML para exploração visual dos resultados.

## Estrutura do projecto

- `notebooks/data_cleaning.ipynb` - limpeza e preparação dos dados.
- `notebooks/abandono_rural_study.ipynb` - análise do abandono rural.
- `notebooks/desenvolvimento_rural_study.ipynb` - análise do desenvolvimento rural.
- `notebooks/programa_de_apoio_ao_interior_study.ipynb` - análise dos programas de apoio ao interior.
- `notebooks/main.ipynb` - recolha automatizada de dados do Arquivo.pt.
- `clean_data/` - ficheiros CSV limpos e prontos a analisar.
- `dados_arquivopt/` - ficheiros em bruto recolhidos por ano.
- `dashboard.html` - dashboard interactivo em HTML.
- `dashboard_data.json` e `dashboard_data.b64` - dados de suporte usados pelo dashboard.

## Principais resultados

O projecto produziu um corpus estruturado sobre narrativas do interior e permitiu identificar:

- os principais drivers do abandono rural, como serviços, factores económicos, ambiente, demografia, cultura e infra-estruturas;
- a diferença entre o modo como a imprensa e as instituições enquadram o tema;
- a evolução temporal das referências ao abandono e ao desenvolvimento rural;
- os beneficiários mais frequentemente associados às políticas de desenvolvimento;
- os sinais de cadeia de valor, sustentabilidade e relevância de política pública;
- um dashboard de síntese para exploração rápida e comunicação dos resultados.

## Como executar a análise

1. Abrir a pasta do projecto no VS Code, Jupyter ou um editor à escolha.
2. Abrir os notebooks dentro da pasta `notebooks/`.
3. Executar `notebooks/main.ipynb` para uma extração de dados à escolha. 
4. Executar `data_cleaning.ipynb` para regenerar os ficheiros limpos em `clean_data/`.
5. Executar depois os notebooks temáticos para rever as análises e gráficos.

## Como descarregar o ficheiro do dashboard

1. Abrir o ficheiro `dashboard.html`.
2. Clicar em **Raw** para ver o ficheiro em bruto.
3. Guardar a página como `dashboard.html` no computador.

Se estiver a trabalhar localmente no VS Code:

1. Abrir directamente o ficheiro `dashboard.html` na raiz do projecto.
2. Se quiser uma cópia fora da pasta do projecto, copiar o ficheiro para outra localização.

Para abrir o dashboard diretamente no navegador (RECOMENDADO)

1. Localizar o ficheiro `dashboard.html`.
2. Fazer duplo clique no ficheiro, ou arrastar o ficheiro para uma janela do browser.
3. Se preferir, usar o menu de contexto do sistema operativo e escolher abrir com Chrome, Edge ou Firefox.

Nota: como o dashboard usa recursos externos, incluindo Chart.js e fontes do Google Fonts, pelo que é recomendável ter ligação à internet para garantir que todos os elementos carregam correctamente.

## Dados e metodologia

O fluxo de trabalho do projecto segue, de forma resumida, estes passos:

1. Pesquisa e recolha de resultados no Arquivo.pt.
2. Normalização de texto, limpeza de snippets e remoção de duplicados.
3. Classificação temática por taxonomias definidas manualmente.
4. Análise de frequências, tendências temporais e comparação entre fontes.
5. Publicação dos resultados em tabelas, gráficos e dashboard.

## Requisitos

- Python 3.x para correr os notebooks.
- Jupyter ou VS Code com suporte para notebooks.
- Navegador moderno para abrir o dashboard.
- Ligação à internet para carregar as dependências externas do HTML.

## Observação final

Este projecto foi concebido para ser exploratório e replicável. A estrutura actual permite acrescentar novos anos de pesquisa, novas palavras-chave ou novos temas sem alterar a lógica central da análise.
