Plano de dados

1. Identificação do projeto

Título: Perfil e inserção dos economistas no mercado de trabalho da Paraíba: diagnóstico para apoiar o Observatório Econômico do CORECON-PB.

Demandante: Conselho Regional de Economia da Paraíba (CORECON-PB).

Equipe: Erika Luciana da Silva, Josiel Matheus da Silva Pereira e Maria Eduarda Sales Bissigo.

Curso: Ciências Econômicas — Universidade Federal da Paraíba (UFPB).

2. Objetivo

Investigar o perfil e a inserção dos economistas no mercado de trabalho da Paraíba, considerando aspectos como formação acadêmica, ocupação, remuneração, distribuição geográfica e setores de atividade, conforme a disponibilidade e a qualidade dos dados.

O estudo pretende produzir um diagnóstico que possa apoiar o CORECON-PB na compreensão do mercado de trabalho relacionado à profissão de economista e contribuir para o planejamento do Observatório Econômico.

3. Fontes de dados

Serão investigadas fontes oficiais e institucionais, considerando sua relevância para os objetivos da pesquisa.

* RAIS — Ministério do Trabalho e Emprego: poderá fornecer informações sobre vínculos formais de trabalho, remuneração, ocupações e características dos estabelecimentos, conforme as variáveis disponíveis.
* PNAD Contínua — IBGE: poderá contribuir para a contextualização do mercado de trabalho, da ocupação e da renda, respeitando os limites de cobertura geográfica e das informações publicadas.
* CORECON-PB: poderão ser consultadas informações institucionais e profissionais disponíveis publicamente. Eventuais solicitações de dados adicionais dependerão de autorização.
* COFECON: poderão ser investigadas informações institucionais relacionadas à profissão e ao sistema de conselhos de Economia.
* MEC/e-MEC e instituições de ensino superior: poderão fornecer informações sobre cursos de Ciências Econômicas e instituições de formação na Paraíba.

As fontes são candidatas e ainda deverão ser avaliadas. A seleção definitiva dependerá da disponibilidade, da cobertura, das variáveis, das condições de acesso e da possibilidade de relacionar as informações ao objetivo da pesquisa.

Links institucionais para consulta:

* RAIS e CAGED: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/acoes-e-programas/programas-projetos-acoes-obras-e-atividades/estatisticas-trabalho/microdados-rais-e-caged
* IBGE — PNAD Contínua: https://www.ibge.gov.br/estatisticas/sociais/trabalho/9171-pesquisa-nacional-por-amostra-de-domicilios-continua.html
* COFECON: https://www.cofecon.org.br/
* MEC/e-MEC: https://emec.mec.gov.br/

O endereço eletrônico do CORECON-PB e os links diretos para suas informações deverão ser confirmados antes de serem registrados como fontes consultadas.

4. Inventário e documentação das fontes

Cada fonte selecionada será documentada no arquivo docs/inventario_fontes.md, contendo:

* Nome da base e instituição responsável;
* Link direto para a página, tabela ou arquivo consultado;
* Cobertura temporal e geográfica;
* Formato dos dados;
* Data efetiva de acesso;
* Licença, restrições e condições de uso;
* Possibilidades e limitações de utilização na pesquisa.

Também serão identificadas, quando disponíveis, a unidade de observação, as chaves de identificação, a periodicidade e as possibilidades de relacionamento entre as bases.

5. Procedimento de aquisição

A aquisição dos dados seguirá as etapas abaixo:

1. Consultar as páginas oficiais das instituições responsáveis.
2. Identificar as bases relacionadas ao objetivo da pesquisa.
3. Verificar a cobertura, o período de referência, as variáveis, o formato e as condições de acesso.
4. Registrar as informações confirmadas no inventário de fontes.
5. Baixar os arquivos ou consultar as tabelas pelos meios oficiais disponíveis.
6. Registrar a data de acesso e preservar os arquivos originais quando permitido.
7. Documentar os procedimentos de limpeza, padronização e transformação dos dados.
8. Registrar as limitações, os erros encontrados e as decisões metodológicas.

Quando não for possível automatizar a aquisição, serão documentadas as etapas manuais necessárias para localizar e obter os dados.

6. Tratamento e análise

Após a seleção das bases, os dados serão avaliados quanto à consistência, à completude e à adequação aos objetivos da pesquisa.

Quando aplicável, poderão ser realizados:

* Verificação de valores ausentes e duplicidades;
* Padronização de nomes de variáveis e categorias;
* Conferência dos tipos e das unidades de medida;
* Identificação de valores inconsistentes;
* Construção de indicadores descritivos de ocupação e remuneração;
* Comparações por período, localização, setor de atividade e características profissionais, conforme a disponibilidade das variáveis.

O relacionamento entre bases somente será realizado quando houver chaves compatíveis e justificativa metodológica. As limitações de comparabilidade serão registradas.

A identificação específica de economistas dependerá da existência de variáveis adequadas, como ocupação ou informações profissionais pertinentes. Não será presumido que todas as bases permitem identificar diretamente essa categoria.

7. Organização e segurança dos dados

O repositório será organizado conforme a estrutura existente no GitHub:

* dados/: organização dos dados da pesquisa;
* docs/: inventário de fontes, dicionário de variáveis e plano de dados;
* notebooks/: códigos e procedimentos de aquisição, tratamento e análise;
* outputs/: tabelas, gráficos e resultados produzidos.

Dentro de dados/, os arquivos originais e os arquivos tratados deverão ser separados em subpastas específicas, como raw/ e processed/, caso essa organização seja adotada no repositório.

Os dados originais serão preservados sem alterações sempre que permitido. Os dados tratados serão produzidos por procedimentos documentados.

Não serão publicados credenciais, senhas, tokens, dados pessoais desnecessários, arquivos restritos ou materiais cuja redistribuição não seja autorizada. Quando uma base não puder ser compartilhada, serão registrados seus meios oficiais de obtenção e os procedimentos necessários para reproduzir a aquisição.

8. Atualização e reprodutibilidade

Para cada base utilizada, serão registrados o período de referência, a data de acesso, a versão disponível e as alterações realizadas durante o tratamento.

A frequência de atualização será definida conforme a periodicidade de cada fonte e a necessidade do Observatório Econômico do CORECON-PB.

Os procedimentos de aquisição e tratamento serão documentados para que outras pessoas possam compreender as etapas realizadas e, quando houver acesso às mesmas fontes, reproduzir a análise.

9. Dicionário de variáveis

O arquivo docs/dicionario_variaveis.md reunirá as variáveis relevantes para a pesquisa, com descrição, tipo de dado, unidade de medida, fonte e cobertura.

O dicionário será atualizado após a seleção e a consulta das bases, de modo que as definições correspondam às variáveis efetivamente disponíveis.

10. Pendências e próximas etapas

* Confirmar as fontes que serão efetivamente utilizadas.
* Verificar os links diretos, a cobertura, o formato e as condições de uso de cada base.
* Registrar as datas reais de acesso no inventário.
* Identificar as variáveis disponíveis e suas limitações.
* Completar o dicionário com base nos dados selecionados.
* Definir os procedimentos de aquisição e atualização de cada fonte.
* Registrar os responsáveis e os prazos das próximas etapas.
* Conferir se a estrutura descrita neste documento corresponde à estrutura efetiva do repositório.
* Preparar os resultados e a documentação para apoiar o diagnóstico solicitado pelo CORECON-PB.
