# Dashboard de RH — Power BI

Painel de indicadores de pessoas em uma página: custo de folha, absenteísmo, headcount, movimentação e perfil demográfico, tudo filtrável por filial, departamento e funcionário.

**Projeto de estudo com dados fictícios.** Nenhuma informação real de empresa ou de pessoa física.

## O problema

RH costuma ter os números, mas espalhados: a folha em uma planilha, o controle de faltas em outra, o quadro de pessoal em uma terceira. A pergunta que o gestor faz — qual filial está com mais falta e quanto isso custa — exige cruzar as três. Este relatório junta tudo em uma tela única, com sete segmentações para recortar por qualquer ângulo.

## O que o painel mostra

| Indicador | Visual |
|---|---|
| Total de funcionários | Cartão |
| Salário por funcionário | Gráfico de barras |
| Salários por filial | Gráfico de colunas |
| Salário por departamento | Gráfico de colunas |
| Quantidade de faltas por filial | Gráfico de colunas |
| Contratações e demissões | Gráfico de área |
| Funcionários por gênero | Rosca |
| Idade por gênero | Rosca |

## Modelo e medidas

A base é uma única tabela, tb_rh, com ID, nome, salário, sexo, departamento, filial, quantidade de faltas, contratações e demissões.

| Medida | Para que serve |
|---|---|
| TOTAL DE SALARIOS | Custo total da folha no recorte filtrado |
| TOTAL_FALTAS | Soma de faltas, base do indicador de absenteísmo |
| GENERO | Contagem de funcionários por gênero |
| IDADE_GENERO | Idade média por gênero |

## Decisões de construção

Tudo em uma página só, de propósito. Indicador de pessoas é consultado em reunião, e trocar de aba no meio da conversa quebra o raciocínio de quem está olhando. As sete segmentações cobrem os recortes que o gestor pede na hora, e os ícones e o plano de fundo foram desenhados para que filial, gênero e média sejam identificáveis sem ler o título do visual.

## Como abrir

Baixe o arquivo Dashboard_RH.pbix e abra no Power BI Desktop. O modelo já vem com os dados importados, não é preciso configurar nenhuma conexão.

## Stack

Power BI Desktop, Power Query (M), DAX.
