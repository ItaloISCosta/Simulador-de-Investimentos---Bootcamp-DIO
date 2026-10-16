# Simulador de Investimentos - Bootcamp DIO

Este repositório contém a planilha de simulação financeira (`TABELA DE INVESTIMENTOS.xlsx`) desenvolvida como desafio de projeto para o bootcamp da [DIO (Digital Innovation One)](https://www.dio.me/). A ferramenta permite simular o crescimento de investimentos ao longo do tempo com base no perfil do investidor.

## 🎯 Perguntas que a ferramenta responde

A ferramenta foi desenhada para responder às seguintes perguntas, ajudando o usuário na tomada de decisão:

* **"Quanto terei acumulado no futuro investindo X por mês?"** 
  * *Onde aparece:* Na célula de "Montante Final" ou "Valor Acumulado" no painel principal.
* **"Qual a rentabilidade esperada para o meu perfil?"** 
  * *Onde aparece:* Na seção de "Taxa de Juros" ou "Rentabilidade" logo após a seleção do perfil.
* **"Como minha carteira deve ser dividida?"** 
  * *Onde aparece:* Na tabela de "Alocação Recomendada" (divisão entre Renda Fixa e Renda Variável).

## 🧮 Como o VF e o PROCV entram nos cálculos

* **PROCV (Procura Vertical):** Utilizado para buscar automaticamente as taxas de rentabilidade anual e a distribuição de ativos com base no **Perfil de Investidor** (Conservador, Moderado ou Arrojado) selecionado no menu suspenso. Ele procura o nome do perfil na matriz de dados e retorna a taxa correspondente.
* **VF (Valor Futuro):** Utilizado para calcular o efeito dos juros compostos. A fórmula recebe a taxa de juros (trazida pelo PROCV e dividida por 12 para conversão mensal), o número de meses (prazo do investimento), o valor do aporte mensal e o valor inicial investido para projetar o patrimônio final.

## 🏷️ Intervalos Nomeados Criados

Para deixar as fórmulas mais limpas, legíveis e fáceis de dar manutenção, criei os seguintes intervalos nomeados na planilha:

* `Perfil_Selecionado`: Célula de entrada onde o usuário escolhe o perfil.
* `Tabela_Perfis`: Matriz onde estão os dados de taxas e percentuais (utilizada na fórmula do PROCV).
* `Aporte_Mensal`: Célula com o valor que será investido todos os meses.
* `Prazo_Meses`: Célula com o tempo total do investimento.

## 📊 Percentuais de cada Perfil e Origem

A distribuição da carteira e as taxas esperadas foram baseadas no material de apoio disponibilizado pelo Expert no Bootcamp da DIO. A divisão de risco ficou estruturada da seguinte forma:

* **Conservador:** 30% FIIs de Papel / 50% FIIs de Tijolo / 10% FIIs Híbridos / 10% FIIs FOFs (Foco em proteção e baixo risco).
* **Moderado:** 32% FIIs de Papel / 35% FIIs de Tijolo / 8% FIIs Híbridos / 5% FIIs FOFs / 10% FIIs de Desenvolvimento / 10% FIIs de Hotelarias (Equilíbrio entre segurança e crescimento).
* **Agressivo:** 50% FIIs de Papel / 10% FIIs de Tijolo / 5% FIIs Híbridos / 5% FIIs FOFs / 20% FIIs de Desenvolvimento / 10% FIIs de Hotelarias (Foco em multiplicação de patrimônio com maior tolerância ao risco).

## 🛠️ O que mudei em relação à ferramenta do Expert

Em relação ao modelo original apresentado nas aulas, implementei as seguintes melhorias na minha `TABELA DE INVESTIMENTOS.xlsx`:

1. **Design e Formatação:** Melhorei a paleta de cores para deixar a interface mais amigável e profissional.
2. **Usabilidade:** Ajustei as células de entrada de dados para ficarem mais intuitivas para o usuário final.

## 📸 Evidências de Funcionamento (Simulações)

Abaixo estão os prints provando o funcionamento dinâmico das fórmulas ao alterar os perfis, mantendo os mesmos valores de aporte e prazo.

### Simulação 1: Perfil Conservador

<img width="726" height="1333" alt="Evidência Perfil Conservador" src="https://github.com/user-attachments/assets/39c60af5-6f1a-4103-aa09-306d9f126ffa" />

### Simulação 2: Perfil Agressivo

<img width="714" height="1353" alt="Evidência Perfil Agressivo" src="https://github.com/user-attachments/assets/4230eb9d-bea1-4cbc-a85e-c4fef7f7f724" />
