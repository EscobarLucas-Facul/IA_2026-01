# Estudo de Trade-off: Segurança da Informação vs Performance de Rede

##Descrição do Projeto
Este projeto analisa o impacto da criptografia (Segurança) nas métricas de fluxo de rede (Performance) utilizando o dataset **CIC-VPN2016**. O objetivo principal é quantificar o overhead introduzido por VPNs e avaliar a eficácia de modelos de Machine Learning (Regressão Logística e Random Forest) na detecção de tráfego criptografado.

O projeto foi desenvolvido como parte dos requisitos acadêmicos para a disciplina de Segurança da Informação, focando no equilíbrio entre proteção de dados e latência de rede.

## Tecnologias Utilizadas
- **Linguagem:** Python 3.x
- **Bibliotecas Principais:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib.
- **Dataset:** [CIC-VPN2016 (Kaggle)](https://www.kaggle.com/datasets/noobbcoder2/vpn-and-non-vpn-application-traffic-cic-vpn2016)
- **Ferramentas:** Google Colab, KaggleHub.

## Estrutura do Notebook
O projeto segue uma estrutura rigorosa de 8 seções:
1. **Título e Objetivo**: Definição do problema.
2. **Dicionário de Dados**: Explicação das variáveis de rede.
3. **Importação e Carregamento**: Setup do ambiente e download via API.
4. **EDA (Análise Exploratória)**: Visualização de correlações e impacto na performance.
5. **Pré-processamento**: Limpeza de outliers e divisão 70/20/10.
6. **Treinamento**: Implementação de RL e Random Forest.
7. **Avaliação**: Comparação de métricas e matrizes de confusão.
8. **Conclusões**: Análise crítica dos resultados.

## Principais Descobertas
- **Eficácia de Detecção:** O modelo **Random Forest** alcançou 100% de Recall, garantindo que nenhum tráfego VPN passasse indetectado.
- **Impacto na Performance:** Identificamos que o tráfego VPN apresenta assinaturas de duração de fluxo e pacotes por segundo significativamente diferentes do tráfego comum.
- **Trade-off:** Enquanto o Random Forest é mais robusto, a **Regressão Logística** mostrou-se 40x mais rápida, sendo ideal para sistemas com recursos limitados.

## Como Executar
1. Clone o repositório.
2. Certifique-se de ter as bibliotecas instaladas: `pip install pandas numpy scikit-learn seaborn kagglehub`.
3. Execute o notebook `projeto_vpn.ipynb` no ambiente Jupyter ou Google Colab.

