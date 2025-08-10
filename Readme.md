# **DataVision BI – Previsões e Detecção de Anomalias na Produção**

## 📌 Sobre o Projeto  
Este projeto tem como objetivo criar dashboards interativos no **Power BI** para **detecção de anomalias** e **projeções de produção futura**, utilizando dados e técnicas aprendidas no curso **Microsoft Power BI Para Business Intelligence e Data Science** da **[Data Science Academy](https://www.datascienceacademy.com.br/)**.  

Como analista de dados, elaborei visualizações que permitem identificar padrões históricos, prever tendências e otimizar decisões estratégicas na gestão da produção.

---

## 🎯 Objetivos e Perguntas de Negócio Respondidas  

1. **Tendência de Produção ao Longo dos Anos**  
   - **Pergunta**: Qual é a projeção da produção total para os próximos 5 anos com base na média anual histórica?  
   - **Benefício**: Antecipar demandas de capacidade, investimentos e recursos humanos.  

2. **Detecção de Desvios Significativos**  
   - **Pergunta**: Em quais anos a produção apresentou desvios relevantes em relação à média histórica?  
   - **Benefício**: Identificar eventos atípicos, problemas operacionais ou oportunidades de melhoria.  

3. **Perfil Etário da Produção**  
   - **Pergunta**: Qual faixa etária apresenta maior produção total no período e como isso varia por turno?  
   - **Benefício**: Compreender o perfil etário mais produtivo e otimizar a alocação de pessoal.  

4. **Impacto do Tempo na Distribuição Etária da Produção**  
   - **Pergunta**: Qual foi a média total de produção por faixa etária (Range de Idade)?  
   - **Benefício**: Otimizar a produção, focando em faixas mais produtivas ou fortalecendo as menos produtivas.  

---

## 📊 Metodologia e Visualizações Utilizadas  

- **Previsão de Produção Futura**  
  - **Gráfico**: Linha com previsão de 5 anos.  
  - **Configuração**: Intervalo de confiança de 75%.  

- **Detecção de Anomalias**  
  - **Gráfico**: Linha com marcação automática de desvios.  
  - **Configuração**: Confiança de 75%.  

- **Produção Média por Faixa Etária**  
  - **Gráfico**: Barras comparando médias por faixa etária.  

- **Evolução da Produção por Ano e Faixa Etária**  
  - **Gráfico**: Área com **drill up** e **drill down** para análise detalhada.  

- **Filtros e Segmentações**: Faixa etária e turno.  

---

## 🧮 Medida DAX Criada  

A única medida personalizada necessária foi o cálculo de **Percentual de Participação**:  

```DAX
Percentual Participação = 
    AVERAGEX(Producao,
        DIVIDE(
            Producao[Total Unidades Produzidas],
            CALCULATE(SUM(Producao[Total Unidades Produzidas]), ALL(Producao))
        )
    ) * 100
```

---

## 🚀 Aprendizados e Experiência  

Durante o desenvolvimento deste projeto:  

- **Aprofundei meu conhecimento em detecção de anomalias** no Power BI, compreendendo como ajustar níveis de confiança para análises mais assertivas.  
- **Entendi como aplicar previsões temporais** para apoiar decisões estratégicas de produção.  
- Aprimorei minhas habilidades em **DAX**, especialmente para criar medidas personalizadas que apresentassem resultados corretos em diferentes contextos visuais.  
- Trabalhei com **drill up e drill down** para permitir análises hierárquicas e flexíveis.  
- Enfrentei desafios na **correta exibição de percentuais** no gráfico 3, exigindo revisões na fórmula DAX para garantir consistência nos valores apresentados.  

Essa experiência foi fundamental para unir teoria e prática, resultando em um dashboard funcional e focado na resolução de problemas reais de negócio.  

---

## 📸 Pré-visualização do Dashboard

![Dashboard Power BI](Dashboard_Previsao_Anomalias_page-0001.jpg)

---

## 📥 Download do Dashboard

Você pode baixar o arquivo completo do dashboard Power BI para abrir e explorar localmente no Power BI Desktop:

[📊 Download Dashboard.pbix](Imagens/Dashboard_Previsao_Anomalias.pbix)

---

## 📚 Créditos  

Todos os dados, conceitos e técnicas utilizados neste projeto foram aprendidos e fornecidos pela **[Data Science Academy](https://www.datascienceacademy.com.br/)** no curso **Microsoft Power BI Para Business Intelligence e Data Science**.  

---

## 🖥️ Ferramentas Utilizadas  

- **Power BI Desktop**  
- **DAX** (Data Analysis Expressions)  
