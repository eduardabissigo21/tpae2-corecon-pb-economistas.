Perfil e inserção dos economistas no mercado de trabalho da Paraíba
Projeto aplicado de extensão da disciplina TPAE II — Técnicas de Pesquisa e Análise Econômica II (PSAE00320), Turma 01, 2026.2, UFPB.
Demandante: Conselho Regional de Economia da Paraíba (CORECON-PB).
Objetivo: produzir um diagnóstico do perfil e da inserção dos economistas no mercado de trabalho formal da Paraíba, para apoiar o Observatório Econômico do CORECON-PB.
Equipe B: Erika Luciana da Silva, Josiel Matheus da Silva Pereira e Maria Eduarda Sales Bissigo.
Situação do projeto
Entrega	Conteúdo	Situação
4	Repositório e plano de dados	Concluída
5	Obtenção, limpeza e tratamento dos dados	Esta versão (notebook, bases tratadas e relatório de qualidade)
Estrutura do repositório
```
notebooks/   código executável do início ao fim (tratamento\_dados\_E05.ipynb)
data/raw/    dados originais, sem edição
data/processed/   bases tratadas (geradas pelo notebook)
outputs/     tabelas de conferência e testes (geradas pelo notebook)
docs/        relatório de qualidade (PDF) e dicionário de dados
```
Fontes de dados
Fonte	Papel	Recorte	Acesso	Situação
RAIS 2024 (Ministério do Trabalho e Emprego)	Estoque anual de vínculos formais	Economistas (CBO 2512) na Paraíba: 233 vínculos	05/11/2026, extração direta do MTE	Tratada
Novo CAGED 2024 (MTE)	Fluxo mensal de admissões e desligamentos	Economistas na Paraíba: 41 movimentações (12 arquivos mensais; dezembro sem registros)	05/11/2026	Tratada
IBGE — DTB	Códigos e nomes dos municípios	223 municípios da Paraíba (data-base 22/11/2024)	05/11/2026	Tratada
INEP — Censo da Educação Superior 2024	Oferta de cursos de Economia	67 linhas de cursos de Economia na PB (22 cursos, 22 IES, 20 municípios)	05/11/2026	Tratada por script próprio (`filtrar\_inep\_cursos.py`)
CORECON-PB	Dados agregados de registrados	—	—	Pendente: depende de autorização e contato
Regra central: a RAIS mede estoque de vínculos e o CAGED mede fluxo de movimentações. As duas bases ficam em tabelas separadas e nunca são somadas.
Como reproduzir
Coloque em `data/raw/` os arquivos:
`rais\_economistas\_pb\_2024.csv`
`caged\_economistas\_pb\_2024.csv`
`RELATORIO\_DTB\_BRASIL\_MUNICIPIO.xls`
Abra `notebooks/tratamento\_dados\_E05.ipynb` (Jupyter, VS Code ou Google Colab).
Execute Reiniciar e executar tudo (Restart & Run All). O notebook não precisa de edição manual e usa caminhos relativos.
Os resultados aparecem em `data/processed/` e `outputs/`.
Requisitos: Python 3, `pandas`, `numpy` e `xlrd` (para ler o `.xls` do IBGE).
> Os arquivos brutos da RAIS e do CAGED têm cerca de 400 MB por arquivo e milhões de linhas, então a extração inicial foi feita em nuvem (Google Colab). O notebook trabalha apenas com os recortes pequenos já filtrados para economistas na Paraíba.
O que o notebook faz
Segue as 7 seções exigidas pelo guia da disciplina:
Objetivo, fontes e produtos.
Bibliotecas e configuração reproduzível.
Leitura dos originais.
Diagnóstico inicial (dimensões, tipos, nulos, duplicatas, valores distintos).
Tratamentos em etapas nomeadas, cada uma com contagem de linhas antes e depois.
Testes de integridade (`assert`) e tabelas de conferência.
Exportação e resumo das decisões.
Principais decisões de tratamento
Tema	Decisão
Nomes de colunas	Padronizados em minúsculas, sem acento e sem espaços.
Colunas com valor único	Removidas da base tratada da RAIS (12 colunas).
Códigos de CNAE	Espaços removidos e lidos como texto.
Ocupação	Filtro pela família 2512 da CBO (7 códigos); códigos lidos como texto de 6 dígitos.
Remuneração igual a zero	Tratada como "não informado", sem imputação; valor original preservado.
Remuneração extrema	Sinalizada pela regra de Tukey (Q3 + 1,5 × IQR) e mantida.
Município	`cod\_ibge6` como chave de junção (a RAIS e o CAGED usam 6 dígitos; o IBGE usa 7).
Junções	Left join com a tabela de municípios; contagens antes e depois conferidas.
Resultados verificados
RAIS 2024: 233 vínculos, 0 duplicatas exatas, 14 municípios, 6 dos 7 códigos da CBO 2512 (não aparece o 251230). Remuneração média nominal: 224 valores positivos, 9 zeros e 20 valores sinalizados como extremos. Remuneração de dezembro ausente em 43 vínculos.
Novo CAGED 2024: 41 movimentações (26 admissões, 15 desligamentos; saldo +11), 7 municípios, 4 códigos de CBO.
Junções: RAIS 233 → 233 e CAGED 41 → 41, sem chaves órfãs.
Testes de integridade: todos aprovados na execução (`outputs/testes\_integridade.csv`).
Os detalhes estão no relatório de qualidade (`docs/E05\_equipeB\_qualidade\_dados.pdf`).
Limitações
Os dados cobrem apenas vínculos formais; os resultados não representam economistas fora do mercado formal.
A RAIS e o CAGED não trazem identificador do trabalhador: as linhas são vínculos ou movimentações, não pessoas.
O CAGED mede fluxo. O saldo de +11 não é a variação do estoque total de economistas.
Com poucos registros (233 na RAIS e 41 no CAGED), médias e contagens por ocupação ou município são sensíveis a poucos casos.
A RAIS apresenta 1 registro com remuneração nominal de R$ 1,10 e valor incompatível em salários mínimos; foi sinalizado, não corrigido.
O Censo da Educação Superior mede a oferta de formação, não a inserção no mercado de trabalho.
Dados pessoais e licenças
O repositório não deve conter dados pessoais, sigilosos ou credenciais. Os recortes da RAIS e do CAGED não trazem nome nem CPF. Dados do cadastro do CORECON-PB, se obtidos, serão usados apenas de forma agregada.
Pendências
Registrar a versão do arquivo da RAIS e o ambiente usado no log de aquisição.
Definir o recorte temporal final (apenas 2024 ou série ampliada).
Confirmar com o CORECON-PB a disponibilidade e as regras de uso do cadastro de registrados.
Conferir os anos de referência dos indicadores do IBGE (alguns rótulos divergem das notas).
Conferir no e-MEC se os 2 cursos presenciais de Economia do Censo 2024 (UFPB e UFCG) correspondem à oferta presencial na Paraíba.
Incluir o tratamento do recorte do INEP no notebook, se a equipe optar por unificar os scripts.
