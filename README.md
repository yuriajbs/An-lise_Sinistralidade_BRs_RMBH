# Diagnóstico Executivo de Segurança Viária — RMBH (2024–2025) 
## 1. Problema de negócio

A gestão da segurança viária na Região Metropolitana de Belo Horizonte (RMBH) enfrenta desafios complexos devido ao elevado fluxo de veículos de carga, tráfego pendular diário entre municípios vizinhos e variações sazonais do clima. As três principais rodovias federais que cortam a região — BR-040, BR-262 e BR-381 — registram um volume expressivo de acidentes com vítimas, gerando custos sociais e operacionais elevados.
Apesar da abundância de dados coletados pelas autoridades de trânsito e concessionárias, os gestores públicos e equipes operacionais careciam de uma ferramenta executiva centralizada que correlacione a acidentalidade com fatores climáticos (pluviometria) e características de tráfego de cada via.
Como Analista/Cientista de Dados, o objetivo deste projeto foi centralizar, organizar e estruturar os principais indicadores estratégicos em uma Dashboard Web Executiva, permitindo tomadas de decisão ágeis e direcionadas para prevenção de acidentes e alocação eficiente de recursos.
Para estruturar o diagnóstico e o plano de ação, a análise foi dividida sob três perspectivas de métricas estratégicas:


Do lado da Infraestrutura e Clima: 
 
  1. Qual a evolução mensal de acidentes em relação à precipitação pluviométrica (mm)? 
  2. Como se comporta a taxa média de acidentes na Estação Seca vs. Estação Chuvosa? 
  3. Qual rodovia concentra o maior volume absoluto e relativo de sinistros? 



Do lado dos Órgãos de Fiscalização e Policiamento: 

  1. Quais trechos e períodos demandam reforço na fiscalização dinâmicas de velocidade (meses secos)? 
  2. Como atuar no período de transição climática ("Primeiras Chuvas")? 
  3. Como proteger grupos vulneráveis (motociclistas) no tráfego pendular diário de trabalho? 

Do lado das Concessionárias de Rodovias: 
  1. Onde priorizar obras preventivas de microfresagem, aderência do asfalto e drenagem? 
  2. Como emitir alertas preventivos eficientes em Painéis de Mensagem Variável (PMVs)? 

O objetivo desse projeto é criar um conjunto de gráficos e/ou tabelas que mostre essas métricas da melhor forma possível para o gestor.

## 2. Premissas assumidas para a análise

  1. Período analisado: Dados consolidados entre 01/01/2024 e 31/12/2025 (24 meses completos); 
  2. Escopo geográfico: Trechos metropolitanos das rodovias federais BR-040, BR-262 e BR-381 na RMBH; 
  3. Sazonalidade climática: Classificou-se como Estação Seca os meses com precipitação acumulada <= 100 mm e Estação Chuvosa os meses com precipitação > 100 mm; 
  4. Visões de negócio: A solução foi estruturada em duas visões complementares: Visão Geral (Diagnóstico Macro) e Visão Detalhada (Testes de Hipóteses e Plano de Ação Estratégico.

## 3. Estratégia da solução 

O  painel interativo foi desenvolvido com duas telas principais focadas na clareza visual e facilidade de leitura para tomadores de decisão:

Visão Geral (Diagnóstico de Sinistros e Pluviometria):  	

  1. KPIs de Impacto Executivo: Total de Sinistros, Sinistros Graves (28,2%), Vítimas Fatais (4,9%) e Taxa de Concentração na BR-381 (58,6%);
  2. Evolução Temporal Mensal: Gráfico comparativo de barras (chuva em mm) e linha (volume de acidentes);
  3. Média Mensal de Acidentes (Estação Seca vs Chuvosa): Comparativo visual direto da média mensal de sinistros por rodovia em cada estação climática. 

Visão Detalhada (Teste de Hipóteses e Plano de Ação):

  1. Matriz de Teste de Hipóteses (H1 a H5): Validação ou refutação estatística de crenças comuns sobre chuva, velocidade e severidade. 
  2. Plano de Ação para Órgãos de Fiscalização: Ações ostensivas para controle de velocidade na seca, operação "Primeira Chuva" e proteção ao tráfego pendular de motociclistas na BR-381. 
  3. Plano de Ação para Concessionárias: Diretrizes de infraestrutura, microfresagem do asfalto, engenharia de drenagem e alertas operacionais em PMVs. 

## 4. Top 3 Insights de dados

  1. O Paradoxo da Estação Seca: O volume total mensal de acidentes não aumenta no período chuvoso (média de 170,1 acidentes/mês na seca vs. 165,3 acidentes/mês na chuva). O asfalto seco leva os motoristas a trafegarem em maiores    velocidades, compensando e igualando o número de ocorrências;

  2. BR-381 como Gargalo Estrutural e Pendular: A BR-381 concentra 58,6% de todos os acidentes da região (2.357 ocorrências). A via é fortemente impactada pelo fluxo diário de trabalhadores entre cidades vizinhas da RMBH e por um    alto volume de acidentes envolvendo motociclistas;

  3. Perigo Crítico nas "Primeiras Chuvas": Os meses de transição (Outubro/Novembro) registram um pico proporcional de gravidade (+13,3% de acidentes graves), pois as primeiras chuvas lavam o óleo e a sujeira acumulados no piso      durante o inverno seco, reduzindo drasticamente a aderência do asfalto. 

## 5. O produto final do projeto

  1. Uma Dashboard Web Executiva e Responsiva, construída em código único HTML/CSS/JavaScript utilizando as bibliotecas Chart.js e FontAwesome.
  2. Autônoma: Não requer instalação de servidores ou softwares adicionais para visualização;
  3. Como visualizar localmente: Basta realizar o download do arquivo dashboard_seguranca_viaria.html e executá-lo com um duplo clique em qualquer navegador web (Chrome, Edge, Firefox, Safari). 

## 6. Conclusão

O objetivo de centralizar as métricas operacionais e climáticas para tomada de decisão foi concluído com sucesso. O diagnóstico provou que a gestão de segurança viária na RMBH não deve ser reativa apenas nos períodos de tempestade, mas sim manter uma estratégia contínua focado no controle de velocidade nos meses secos e na fiscalização de motociclistas e tráfego pendular nos corredores urbanos da BR-381. 

## 7. Para o futuro

  1. Granularidade Diária/Horária: Incorporar dados no nível diário para analisar picos específicos durante tempestades pontuais de verão;
  2. Georreferenciamento: Integrar mapas interativos (ex: Leaflet.js / Folium) para mapeamento exato dos blackspots (quilômetros mais críticos);
  3. Análise Preditiva: Desenvolver modelos de Machine Learning para prever a probabilidade de acidentes graves com base na previsão meteorológica diária. 
