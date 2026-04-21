#  Dashboard de Análise de Dados de RH com Power BI

Este repositório contém um projeto de Business Intelligence focado na análise do quadro de funcionários de uma empresa. O objetivo é fornecer insights rápidos sobre demografia, cargos, engajamento e disponibilidade para horas extras, auxiliando a tomada de decisão estratégica do setor de RH.

#  📊 Visão Geral do Dashboard
O relatório foi desenvolvido no Power BI e apresenta as seguintes métricas principais:

**Total de Funcionários:** Contagem total do quadro ativo.

**Experiência Média:** Média de anos de experiência dos colaboradores.

**Distribuição por Gênero:** Divisão percentual e numérica entre homens e mulheres.

**Média Salarial:** Valor médio dos salários mensais.

**Distribuição por Função:** Gráfico de barras identificando os cargos com maior volume de pessoas (ex: Cientista de Dados, Analista de Dados).

**Envolvimento no Trabalho:** Nível de engajamento segmentado (Médio, Baixo, Alto, Ruim).

**Disponibilidade para Horas Extras:** Percentual de funcionários aptos a realizar jornada estendida.

<p align="center">
  <b>Visão 1: Perfil do Cliente e Demografia</b><br>
  <img src="img/Análise de Dados de RH com Power BI.JPG" alt="Visão Cliente" width="800">
  
</p
  
# 🛠️ Tecnologias e Ferramentas

**Power BI:** Criação do dashboard e visualização de dados.

**DAX (Data Analysis Expressions):** Linguagem utilizada para a criação de medidas personalizadas.

**Power Query:** Para limpeza e transformação dos dados (ETL).

#  🧮 Fórmulas DAX Utilizadas
Neste projeto, foram criadas medidas específicas para garantir a precisão dos cálculos dinâmicos. Abaixo estão alguns exemplos de fórmulas aplicadas:

Total de Funcionários (Contagem):

```
TabelaFuc = COUNTROWS(DatasetRH)
```

Total Feminino:

```
TotalFeminino = CALCULATE([TabelaFuc], DatasetRH[Genero] = "Feminino")
```

Percentual de Gênero Feminino:

```
% Genero Feminino = 
DIVIDE(
    [TotalFeminino], 
    [TabelaFuc], 
    0
)
```

Média Salarial:

```
Media Salarial = AVERAGE(DatasetRH[Salario_Mensal])
```

#  📈 Principais Insights
**Concentração Técnica:** A maioria dos funcionários ocupa cargos voltados a dados, com destaque para a função de Cientista de Dados.

**Equilíbrio de Gênero:** A força de trabalho é composta por aproximadamente 60% homens e 40% mulheres.

**Engajamento:** O nível de envolvimento Médio é o predominante (59%), indicando uma oportunidade para programas de motivação e retenção.

**Horas Extras:** A grande maioria (71,57%) não está disponível para horas extras, o que pode impactar o planejamento de projetos urgentes.

#  🚀 Como visualizar o projeto
Baixe o arquivo .pbix disponível neste repositório.

Abra o arquivo no Power BI Desktop.

Caso os dados não carreguem, verifique o caminho da fonte de dados no Power Query.
