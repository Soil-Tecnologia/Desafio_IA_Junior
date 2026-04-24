## Como iniciar

> Este repositório deve ser usado apenas como base inicial do desafio.  
> A entrega deve ser feita em um **novo repositório privado** no GitHub, preservando a estrutura solicitada e compartilhado com os avaliadores ao final.

Para iniciar o desafio, siga o fluxo abaixo:

1. Clone este repositório base:
   ```bash
   git clone <url-do-repositorio-base>
   cd <nome-do-repositorio>
   ```

2. Crie um **novo repositório privado** no seu GitHub.

3. Remova o `origin` atual:
   ```bash
   git remote remove origin
   ```

4. Adicione o seu novo repositório privado como `origin`:
   ```bash
   git remote add origin <url-do-seu-repositorio-privado>
   ```

5. Suba o código para o seu repositório:
   ```bash
   git push -u origin main
   ```

6. Ao final do desafio, compartilhe o acesso ao repositório privado com os avaliadores.

# Desafio Técnico — Engenheiro de ML/IA Júnior

Seu desafio é, a partir de **3 datasets**, construir um **único dataset final** para o treinamento de um modelo capaz de **prever precipitação de chuva** para um local definido a partir dos dados fornecidos.

## Datasets disponíveis

### CEMADEN
Dataset de pluviometria contendo medições de pluviômetros em diversas cidades do estado de Minas Gerais.  
Cada arquivo dentro da pasta `CEMADEN` representa um **mês do ano de 2024**.

### INMET
Dataset meteorológico contendo dados climáticos de diferentes cidades do estado de Minas Gerais.  
Cada arquivo representa uma **cidade no ano de 2024**.

### NASA POWER
Dataset de medições satelitais obtido via API.

A documentação para requisição dos dados da NASA está disponível em:  
<https://power.larc.nasa.gov/docs/services/api/temporal/hourly/>

Os parâmetros obrigatórios a serem extraídos da NASA são:

- `PRECTOT`
- `PS`
- `ALLSKY_SFC_SW_DWN`
- `T2M`
- `T2MDEW`
- `RH2M`
- `WS10M`
- `WD10M`
- `U10M`
- `V10M`
- `QV2M`
- `T2MWET`

## Requisitos obrigatórios

- É obrigatório utilizar informações provenientes dos **três datasets** na construção do dataset final.
- É obrigatório utilizar a coluna `valorMedida` do CEMADEN como base da variável **target**.
- É obrigatório construir um **único dataset final**, pronto para modelagem.
- É obrigatório treinar **ao menos um modelo de predição**.
- É obrigatório fornecer um arquivo `requirements.txt` consistente com a solução entregue, permitindo a reprodução do ambiente utilizado.

## Análises e saídas obrigatórias

Além da construção do dataset e do treinamento do modelo, sua entrega deve conter, no mínimo:

- análise de valores nulos do dataset final;
- análise dos tipos das colunas do dataset final;
- distribuição da variável target;
- matriz de correlação entre as variáveis numéricas do dataset final;
- correlação das variáveis com a target;
- tabela com métricas do modelo, contendo no mínimo:
  - `MAE`
  - `MSE`
  - `RMSE`
  - `R²`
- gráfico mostrando a evolução de alguma métrica de erro ou curva de treinamento, quando aplicável ao modelo escolhido;
- gráfico comparando valores reais e previstos;
- análise de importância das features, quando aplicável ao modelo escolhido;
- curvas de treino e validação, quando aplicável ao modelo escolhido.

## Entrega

A entrega deve ser realizada por meio de um repositório no GitHub. A organização dos arquivos deve, obrigatoriamente, seguir a estrutura abaixo:

```text
orig/
data/
src/
output/
reports/
README.md
requirements.txt
```

## Observações

Fica a critério do candidato definir:

- a estratégia de tratamento e integração dos dados;
- o horizonte de previsão, desde que seja de no mínimo **24 horas** e justificado tecnicamente;
- as colunas utilizadas;
- as transformações aplicadas;
- o modelo adotado.

A documentação da entrega deve permitir compreender com clareza os critérios adotados ao longo da construção do dataset e do modelo.

**A avaliação considerará não apenas o desempenho final do modelo, mas também a coerência metodológica, a qualidade da construção do dataset, a capacidade de sustentar tecnicamente as decisões tomadas, o uso adequado de Git, a organização do repositório, a clareza do código e a reprodutibilidade da solução.**

## Contato

Em caso de dúvidas sobre o desafio, entre em contato pelo WhatsApp:

**WhatsApp:** +55 35 9884-2597