# Projeto Tech Challenge Fase 1 - Análise de NPS no E-commerce

Esse projeto foi desenvolvido para a entrega individual da Fase 1 do Tech Challenge. O objetivo principal é analisar os dados de um e-commerce para entender o que faz a nota de satisfação do cliente (NPS) subir ou cair, e como a operação da empresa pode melhorar antes de o cliente ficar insatisfeito.

---

## Estrutura do Repositório

* **data/**: pasta onde está o arquivo com os dados dos pedidos (desafio_nps_fase_1.csv).
* **notebooks/**: pasta onde está o arquivo de código em Python (EDA_NPS.ipynb).
* **README.md**: este arquivo com o resumo e as explicações do trabalho.

---

## 1. Entendimento do Negócio

* **Problema que estamos resolvendo:** Hoje a empresa só descobre que o cliente teve uma experiência ruim no final de tudo, quando envia a pesquisa. A ideia aqui é olhar os dados do processo (como tempo de entrega e contatos no suporte) para entender a causa das notas baixas e agir antes.
* **Por que o NPS é importante:** No e-commerce é muito fácil o cliente trocar de loja. Manter um cliente antigo sai mais barato do que trazer um novo, e notas baixas mostram que a empresa corre risco de perder vendas futuras.
* **Áreas beneficiadas:** A área de Logística (para ajustar prazos), o Atendimento (para resolver problemas mais rápido) e a área de Pricing/Produto (para checar a percepção sobre o frete).

### Impacto no negócio
* **Recompra:** Cliente insatisfeito (detrator) praticamente não volta a comprar na loja no mês seguinte, enquanto o cliente satisfeito (promotor) compra de novo.
* **Boca a boca:** Clientes que gostam do serviço indicam para conhecidos. Já os insatisfeitos costumam reclamar em redes sociais e sites de opinião, o que afasta novos compradores.
* **Market share:** Para a empresa crescer no mercado de e-commerce, ela precisa conseguir reter a base atual de clientes enquanto atrai novos.

---

## 2. Definição da Target

* **Variável escolhida:** `nps_score` (que foi dividida em Detrator, Neutro e Promotor).
* **Por que escolhi:** É a variável que traz diretamente a nota que o cliente deu para a experiência dele.
* **Quando é coletada:** No fim da jornada, depois que o produto já foi entregue e o atendimento finalizado.
* **Cuidados:** O risco é focar só nessa nota no final do mês e esquecer de acompanhar os indicadores do dia a dia (como atrasos e tempo de resposta no suporte).

---

## 3. Principais Achados da Análise (EDA)

Ao analisar a base de dados no Python, cheguei às seguintes conclusões:

1. **Atraso na entrega:** É o fator que mais prejudica a nota. O cliente tolera o tempo de frete normal, mas quando a entrega passa do prazo combinado, a nota cai drasticamente.
2. **Problemas no suporte:** Os clientes com notas baixas precisaram falar com o atendimento quase 2 vezes e esperaram por volta de 6 dias para ter um retorno.
3. **Situação da base:** A maioria da base (74%) é composta por detratores, o que mostra que a operação precisa ajustar urgente o cumprimento dos prazos e o suporte.
4. **Recompra:** Na análise deu para ver que quase 100% dos clientes promotores voltam a comprar em 30 dias, enquanto o grupo de detratores não faz novas compras.

---

## Como abrir o projeto

Para testar o código:
1. Abra o arquivo `notebooks/EDA_NPS.ipynb` no Google Colab.
2. Carregue a base de dados `data/desafio_nps_fase_1.csv`.
3. Rode as células para visualizar os dados e os gráficos gerados.
