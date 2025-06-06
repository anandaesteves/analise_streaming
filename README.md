# Análise Comparativa de Catálogos de Plataformas de Streaming

## 1. Visão Geral do Projeto
Este projeto realiza uma análise de dados sobre o catálogo de filmes e séries de quatro grandes plataformas de streaming: **Netflix, Prime Video, Max e Apple TV**. Atuando como uma consultoria de mídia e entretenimento, o objetivo é gerar insights sobre padrões de conteúdo, engajamento e tendências de mercado.

A análise visa responder a perguntas de negócio que podem orientar equipes de aquisição de conteúdo, marketing e desenvolvimento de algoritmos de recomendação.

## 2. Objetivos da Análise
O estudo foi guiado pelas seguintes perguntas de negócio:
-   Identificar quais plataformas concentram os títulos com as melhores avaliações.
-   Analisar se há diferença de foco entre gêneros por plataforma.
-   Verificar o perfil médio dos títulos (ano de lançamento, gênero, nota) em cada serviço.
-   Determinar qual plataforma investe mais em clássicos e qual foca em lançamentos recentes.
-   Avaliar pontos fortes e oportunidades de melhoria para a Netflix em comparação com os concorrentes.

## 3. Ferramentas e Bibliotecas
A análise foi desenvolvida em um ambiente Jupyter Notebook utilizando as seguintes bibliotecas Python:
-   **Pandas:** Para manipulação e limpeza dos dados.
-   **Matplotlib & Seaborn:** Para a criação de visualizações e gráficos.

## 4. Fonte de Dados
Os dados foram extraídos de quatro arquivos CSV distintos, cada um representando o catálogo de uma plataforma:
-   `data_netflix.csv`
-   `data_prime_video.csv`
-   `data_hbo_max.csv`
-   `data_apple_tv.csv`

As principais colunas utilizadas na análise foram: `title`, `type`, `releaseYear`, `genres`, `imdbAverageRating` e `imdbNumVotes`.

## 5. Metodologia
O projeto seguiu as seguintes etapas:
1.  **Carga e Consolidação:** Os quatro arquivos CSV foram carregados e consolidados em um único DataFrame, com uma coluna adicional (`platform`) para identificar a origem de cada título.
2.  **Pré-processamento e Limpeza:**
    -   Remoção de registros com dados essenciais ausentes (título, gênero, nota e votos).
    -   Tratamento de valores nulos e remoção de títulos duplicados por plataforma.
    -   Conversão de tipos de dados para garantir a consistência nas análises.
    -   Processamento da coluna de gêneros para permitir a análise individual de cada gênero listado.
3.  **Análise Exploratória Comparativa:** Foram gerados gráficos e métricas para comparar as plataformas, focando em volume de catálogo, proporção de filmes vs. séries, avaliação média e distribuição de lançamentos.
4.  **Análise Específica (Netflix):** Foi realizado um aprofundamento no catálogo da Netflix para identificar seus gêneros mais populares, analisar títulos "Evergreen" e avaliar a qualidade de seu conteúdo ao longo do tempo.

## 6. Principais Insights e Conclusões

### Análise Comparativa entre Plataformas
-   **Volume de Catálogo:** O **Prime Video** possui o maior catálogo em termos de quantidade de títulos, com uma margem significativa sobre os concorrentes.
    
    *Visualização Associada: Gráfico de Barras - "Total de Títulos por Plataforma de Streaming"*
-   **Proporção de Filmes vs. Séries:** Todas as plataformas focam majoritariamente em filmes. O **Prime Video** tem a maior proporção (88% filmes), enquanto a **Max** apresenta o catálogo mais equilibrado (67% filmes e 33% séries), sugerindo uma estratégia de conteúdo mais diversificada.
    
    *Visualização Associada: Gráfico de Barras Empilhadas - "Proporção de Filmes e Séries por Plataforma"*
-   **Qualidade vs. Popularidade:**
    -   A **Max** lidera em **qualidade**, com a maior média de avaliação IMDb (6.80) para títulos com mais de 1000 votos. A plataforma também se destaca na **popularidade** (média de votos), indicando que seu catálogo, embora menor, contém títulos de grande engajamento.
    -   A **Netflix** aparece em segundo lugar em qualidade (nota média de 6.60), demonstrando um bom equilíbrio entre volume e curadoria.
    
    *Visualizações Associadas: Gráficos de Barras - "Média de Avaliação IMDb" e "Média de Votos IMDb"*
-   **Foco em Lançamentos:** Todas as plataformas mostram uma clara tendência de focar em conteúdo pós-2000. **Netflix e Prime Video** possuem um catálogo com um pico acentuado em produções mais recentes (a partir de 2010), indicando uma estratégia focada em novidades e tendências.

    *Visualização Associada: Histograma - "Distribuição do Ano de Lançamento por Plataforma"*

### Análise Específica - Netflix
-   **Perfil do Catálogo:** A nota média dos títulos da Netflix (6.40) está ligeiramente acima da média geral das plataformas (6.39). Suas **séries (nota média 7.04)** são notavelmente mais bem avaliadas que seus **filmes (6.21)**.
-   **Gêneros Populares:** Os gêneros de maior destaque na plataforma são **Comédia** e **Drama**.
-   **Títulos "Evergreen":** A Netflix possui em seu catálogo títulos clássicos de alta aclamação e popularidade, como **"Breaking Bad"**, **"Band of Brothers"** e **"Avatar: The Last Airbender"**, que funcionam como fortes atrativos para retenção de assinantes.

## 7. Como Executar o Projeto
Para reproduzir esta análise, siga os passos abaixo:

1.  **Pré-requisitos:**
    -   Python 3
    -   Jupyter Notebook ou qualquer IDE compatível.

2.  **Instalação das Bibliotecas:**
    ```bash
    pip install pandas matplotlib seaborn
    ```

3.  **Estrutura de Arquivos:**
    -   Certifique-se de que os arquivos CSV (`data_netflix.csv`, etc.) estejam na mesma pasta do notebook ou em um subdiretório.

4.  **Execução:**
    -   Abra o arquivo `Trabalho Python Digital College.ipynb`.
    -   Execute as células sequencialmente para replicar a análise e gerar os gráficos.
