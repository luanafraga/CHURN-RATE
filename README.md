# CHURN-RATE

**Análise da Taxa de Evasão de Clientes (Churn Rate)**

O projeto foi desenvolvido utilizando linguagem **Python** no Jupyter Notebook. O python possui um série de bibliotecas que nos auxiliam na construção das análises e modelagem dos dados. Neste projeto, foram utilizadas as seguintes:

   - Pandas
   - Numpy
   - Seaborn
   - Matplotlib
   - Imbalanced-learn
   - Scikit-learn

**Objetivo**

O objetivo deste projeto é **Avaliar e reduzir a Taxa de Evasão de Clientes**, conhecido como Churn Rate. Basicamente, o Churn Rate indica o quanto a empresa perdeu de receita ou clientes em um período de tempo.

Como passo inicial, é necessária a **identificação de clientes que teriam uma maior chance de deixar a empresa.** Para isso, é interessante investigar algumas características de clientes para tentar classificar estas pessoas como potenciais candidatas a deixar a empresa ou não.

**Dados**

A base de dados possui informações sobre:

- **Cliente:**
    - **CustomerID:** número de identificação do cliente
    - **Churn:** se o cliente deixou ou não a empresa
    - **Gender:** gênero (masculino e feminino)
    - **SeniorCitizen:** informação sobre um cliente ter ou não idade igual ou maior que 65 anos
    - **Partner:** se o cliente possui ou não um parceiro ou parceira
    - **Dependents:** se o cliente possui ou não dependentes
    
    
- **Serviço de telefonia:**
    - **Tenure:** meses de contrato do cliente
    - **PhoneService:** assinatura de serviço telefônico
    - **MultipleLines:** assisnatura de mais de uma linha de telefone
    
    
- **Serviço de internet:**
    - **InternetService:** assinatura de um provedor internet
    - **OnlineSecurity:** assinatura adicional de segurança online
    - **OnlineBackup:** assinatura adicional de backup online
    - **DeviceProtection:** assinatura adicional de proteção no dispositivo
    - **TechSupport:** assinatura adicional de suporte técnico, menos tempo de espera
    - **StreamingTV:** assinatura de TV a cabo
    - **StreamingMovies:** assinatura de streaming de filmes
    
    
- **Contrato:**
    - **Contract:** tipo de contrato
    - **PaperlessBilling:** se o cliente prefere receber online a fatura
    - **PaymentMethod:** forma de pagamento
    - **Charges.Monthly:** total de todos os serviços do cliente por mês
    - **Charges.Total:** total gasto pelo cliente


**Conclusões**


Após o pré-processamento dos dados, foram criados 4 modelos de machine learning com a biblioteca Scikit Learn: Regressão Logística, SVC, Árvore de decisão e Random Forest. Esses modelos foram treinados e avaliados utilizando métricas de avaliação matemáticas e gráficas, para a escolha do melhor modelo. O modelo **Regressão Logística** apresentou o melhor resultado nas métricas analisadas.

Por fim, conseguimos também detectar alguns padrões de clientes que **tendem a cancelar o contrato** com a empresa:


   - Menores de 65 anos;
   - Sem cônjuge e dependentes;
   - Contrato menor que 10 meses;
   - Com serviço de fibra ótica;
   - Sem servicos complementares (segurança online, backup online, proteção de dispositivo, suporte técnico);
   - Com contrato mensal;
   - Com método de pagamento via boleto eletrônico;
    
**Sugestão de projetos de ação:**

   - Podemos realizar **promoções** para:
        - O cliente trasnferir o prazo de seu contrato para o **anual**;
        - Adquirir **serviços complementares**;
        - Adquirir uma **linha adicional** para familiar;
   - Pensar em alguma ação para os clientes migrarem do método de pagamento boleto para outra, como **cartão de crédito**;
   - Verificar qual o problema dos clientes que possuem fibra ótica e agir em cima deste problema.
