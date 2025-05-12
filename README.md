# Análise dos Impactos Socioeconômicos do Desmatamento no Pará

Este projeto analisa os impactos socioeconómicos do desmatamento no estado do Pará, Brasil. Utiliza dados de desmatamento (PRODES), Produto Interno Bruto (PIB) municipal, produção da extração vegetal e indicadores de governança (CGU) para explorar as correlações e tendências.

O principal resultado é um notebook Jupyter (`analise_desmatamento_para_final_executado.ipynb`) que documenta todo o processo de aquisição, limpeza, transformação, fusão de dados e análise exploratória, incluindo visualizações e interpretações.

## Conteúdo do Repositório

-   `analise_desmatamento_para_final_executado.ipynb`: O notebook Jupyter principal com toda a análise.
-   `dados_analise_desmatamento_pa.csv`: O conjunto de dados consolidado e processado, utilizado no notebook.
-   `meu_banco.db`: O banco de dados SQLite original (necessário para executar a secção de carga de dados do notebook, caso queira refazer desde o início).
-   Imagens (gráficos gerados pela análise):
    -   `dist_desmatamento.png`
    -   `evolucao_desmatamento.png`
    -   `desmatamento_pib.png`
    -   `evolucao_temporal_detalhada.png`
-   `README.md`: Este ficheiro.

## Como Executar o Notebook

1.  **Ambiente:**
    *   Certifique-se de que tem Python 3.8+ instalado.
    *   Recomenda-se o uso de um ambiente virtual (por exemplo, venv ou conda).

2.  **Dependências:**
    Instale as bibliotecas Python necessárias. Pode instalá-las usando pip:
    ```bash
    pip install jupyter pandas numpy matplotlib seaborn nbformat ipykernel
    ```
    (Nota: `sqlite3` geralmente já vem incluído na instalação padrão do Python.)

3.  **Jupyter Notebook:**
    *   Se ainda não o fez, instale o Jupyter Notebook ou JupyterLab:
        ```bash
        pip install notebook
        # ou para JupyterLab
        # pip install jupyterlab
        ```
    *   Navegue até ao diretório do projeto no seu terminal.
    *   Inicie o Jupyter Notebook/Lab:
        ```bash
        jupyter notebook
        # ou
        # jupyter lab
        ```
    *   Abra o ficheiro `analise_desmatamento_para_final_executado.ipynb` no seu navegador.

4.  **Execução das Células:**
    *   O notebook fornecido (`analise_desmatamento_para_final_executado.ipynb`) já contém todos os outputs da execução. 
    *   Se desejar re-executar as células, pode fazê-lo individualmente ou selecionar "Kernel" > "Restart & Run All" no menu do Jupyter.
    *   **Importante**: Para a secção de carga de dados original funcionar (primeiras células de código que leem do `meu_banco.db`), o ficheiro `meu_banco.db` deve estar no local esperado pelo notebook (originalmente `/home/ubuntu/upload/meu_banco.db`). Se o moveu, precisará de ajustar o caminho no código da célula correspondente ou colocar o ficheiro `meu_banco.db` na mesma pasta do notebook e ajustar o caminho para `db_path = 'meu_banco.db'`.
    *   O ficheiro `dados_analise_desmatamento_pa.csv` é gerado pelo notebook. Se este ficheiro já existir e executar o notebook novamente, ele será sobrescrito.

## Descrição do Projeto

O objetivo deste trabalho foi avaliar os impactos socioeconómicos do desmatamento no estado do Pará. O processo envolveu:

1.  **Aquisição de Dados:** Carregamento de dados de múltiplas tabelas de um banco de dados SQLite.
2.  **Limpeza e Transformação:** Tratamento de valores ausentes, conversão de tipos de dados e filtragem para o estado do Pará.
3.  **Fusão de Dados:** Combinação das diferentes fontes de dados num único DataFrame consolidado.
4.  **Análise Exploratória de Dados (AED):** Geração de estatísticas descritivas e visualizações para identificar padrões, tendências e correlações entre desmatamento, PIB, extração vegetal e indicadores de governança.
5.  **Interpretação:** Discussão dos resultados e dos potenciais impactos socioeconómicos.

## Contribuições

Este projeto foi desenvolvido como parte de um desafio de ciência de dados. O foco principal foi na manipulação, análise e visualização de dados para responder a uma pergunta específica sobre os impactos do desmatamento.

