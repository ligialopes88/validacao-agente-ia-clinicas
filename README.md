# Validação de demanda: agente de IA para o WhatsApp de clínicas odontológicas

**Case de Product Discovery · Metodologias Ágeis e Validação de Produtos · UniFECAF**
Parte Prática: experimento real de validação · Lígia Lopes

🎥 **Vídeo pitch:** [assistir no YouTube](https://youtu.be/QTX9iRVXw8Y)
📄 **Parte Teórica:** [docs/Parte-Teorica.pdf](docs/Parte-Teorica.pdf)

---

## 1. Resumo

Testei se clínicas odontológicas de São Paulo têm o problema de demorar a atender pacientes no WhatsApp, e se teriam interesse em um agente de IA que responde na hora, agenda a avaliação e passa o paciente para a equipe.

Em **26 e 27/10/2026** contatei **20 clínicas odontológicas** pelo WhatsApp. Em 18 delas, primeiro fiz uma pergunta como paciente (sobre clareamento), para observar o atendimento real. Depois me identifiquei e apresentei a proposta.

- **Problema observado:** das 6 clínicas consultadas à noite, **5 só continuaram o atendimento na manhã seguinte**. Em horário comercial, **7 de 12** demoraram 19 minutos ou mais, só mandaram mensagem automática, ou não responderam no mesmo dia.
- **Reação à proposta:** **7 clínicas responderam**. **1 testou a demonstração e gostou**, **1 está conversando** sobre como retoma pacientes hoje, e **5 recusaram ou levantaram objeções**. Nenhuma aceitou pagar até agora.
- **Primeiro feedback do protótipo:** a clínica que testou achou o agente útil justamente para **atender quando a equipe não está online e não perder vendas**.

**Decisão: ajustar.** A dor do atendimento fora do horário existe, foi observada e foi o valor que a única clínica que testou enxergou. A demanda pela solução, do jeito que foi apresentada, ainda é fraca.

---

## 2. Problema, público e oportunidade

- **Problema (hipótese):** pacientes mandam mensagem pedindo informação e preço. Se a resposta demora ou chega fora do horário, o paciente pode desistir ou sumir depois de saber o valor.
- **Público:** clínicas odontológicas pequenas e médias em São Paulo capital, com recepção enxuta.
- **Oportunidade:** um agente de IA responde na hora, inclusive à noite, tira dúvidas básicas, agenda a avaliação e entrega o paciente para a equipe.
- **Origem da hipótese:** minha experiência de 15 anos em atendimento ao cliente, e não uma pesquisa prévia com clínicas. Por isso ela precisava ser testada antes de qualquer construção.

---

## 3. Hipóteses e critérios de sucesso

Os critérios abaixo foram definidos em **05/10/2026, antes dos contatos**.

| # | Hipótese | Critério definido antes | Resultado | Status |
|---|---|---|---|---|
| H1 | **Problema:** clínicas perdem pacientes por demora na resposta ou porque o paciente some depois de perguntar o preço | Pelo menos 4 de 5 respondentes relatam já ter perdido pacientes assim | A demora foi **observada** (5 de 6 à noite, 7 de 12 em horário comercial). Nenhuma clínica **relatou** perder pacientes. 1 confirmou que tem um jeito de retomar quem some. | **Parcialmente apoiada** |
| H2 | **Solução:** as respostas do agente são avaliadas como úteis | Pelo menos 3 de 5 dão nota 4 ou 5 | 1 clínica testou a demonstração e avaliou positivamente (útil para atender fora do horário e não perder vendas). Sem nota numérica, e só 1 de 5 avaliações previstas. | **Primeiro sinal positivo, amostra insuficiente** |
| H3 | **Valor:** a clínica pagaria ou pediria uma versão | Pelo menos 2 de 5 aceitam pagar ou pedem uma versão | 0 de 7 que responderam. 1 testou e gostou, mas não falou em pagar. | **Não confirmada** |

**Regra de decisão definida antes do teste**

- **Perseverar:** H1, H2 e H3 confirmadas.
- **Ajustar:** a dor existe, mas a solução foi mal avaliada ou a oferta precisa mudar.
- **Pivotar:** a dor existe e a solução agrada, mas ninguém quer pagar. Muda o segmento ou o modelo.
- **Abandonar:** a dor não aparece.

---

## 4. Lean Canvas

| Bloco | Hipótese inicial (testada) | Ajuste após a rodada |
|---|---|---|
| **Problema** | 1) Paciente pergunta o preço, a resposta demora e ele some. 2) A recepção repete as mesmas respostas. 3) Fora do horário ninguém responde. | O problema 3 foi o mais visível. O problema 1 continua sem confirmação direta das clínicas. |
| **Alternativas existentes** | Não mapeadas | Algumas clínicas **já usam IA** no atendimento. Outras usam mensagem automática de ausência. |
| **Segmento de clientes** | Clínicas odontológicas em SP | Clínicas **sem automação**, com atendimento humano só em horário comercial |
| **Proposta de valor** | Responda todo paciente na hora, 24h | **Apoio à recepção fora do horário**: o agente acolhe, agenda e a equipe continua de manhã. Não substitui o atendimento humano. |
| **Solução** | Agente de IA no WhatsApp com respostas e agendamento | Mesma base, com passagem fácil para humano, sem preço fechado e com o tom da clínica |
| **Canais** | Teste como paciente + proposta por WhatsApp | Conversa de descoberta, sem teste oculto (abordagem já mudada em 28/10) |
| **Receita** | Mensalidade (valor não validado) | Piloto de 7 dias antes de falar de preço |
| **Custos** | Plataforma de automação, API de IA, API do WhatsApp, tempo de configuração | Sem mudança |
| **Métricas** | Taxa de resposta, demonstrações aceitas, disposição de pagar | Tempo de primeira resposta humana, % que confirma perder pacientes, nota da demonstração |
| **Vantagem competitiva** | Agente configurado com as respostas reais de cada clínica | Mesmo, mais experiência em atendimento e foco em manter o toque humano |

---

## 5. Experimento realizado

**Tipo:** teste de demanda em duas etapas, feito antes de construir o produto final.

**Como foi feito**

1. Levantei clínicas odontológicas de São Paulo no Google Maps e registrei tudo numa base no Notion (status, data, tempo de resposta, observações).
2. **Etapa 1, observação do atendimento:** em 18 clínicas, mandei uma pergunta como paciente ("vocês fazem clareamento? como funciona? qual o valor?"). Foram 6 à noite (26/10, cerca de 21h) e 12 em horário comercial (27/10, terça, 17h09). Anotei o tempo até a primeira resposta e quem respondeu (automático ou pessoa).
3. **Etapa 2, proposta:** depois me identifiquei, expliquei o motivo do contato e ofereci uma demonstração de 15 minutos. Em 2 clínicas a abordagem foi direta, sem a etapa 1.
4. **Protótipo:** montei um agente de demonstração no ElevenLabs para uma clínica fictícia (ver apêndice) e enviei o link a quem aceitou ver.

**Limitações, ditas com clareza**

- A janela foi curta: 8 clínicas foram contatadas na tarde de 27/10 e ainda podem responder.
- O teste como paciente mede **demora**, não **perda de pacientes**. A perda continua dependendo do relato das clínicas.
- O protótipo roda fora do WhatsApp (no ElevenLabs) e foi avaliado por uma única clínica, sem nota numérica.
- A etapa 1 seguida de revelação incomodou parte das clínicas (seção 7). Isso afetou as respostas da etapa 2.

---

## 6. Evidências obtidas

Os nomes das clínicas e das pessoas foram omitidos por privacidade (LGPD). Os registros completos de cada conversa (data, horário, quem respondeu e o que disse) estão na base de acompanhamento mantida no Notion.

**Etapa 1: atendimento ao paciente (18 clínicas)**

| Quando a pergunta foi enviada | O que aconteceu |
|---|---|
| **À noite** (26/10, cerca de 21h), 6 clínicas | 5 de 6 só continuaram o atendimento **na manhã seguinte**, 3 delas depois de mensagem automática de ausência. 1 respondeu em 45 minutos. |
| **Horário comercial** (27/10, 17h09), 12 clínicas | 5 de 12 responderam com uma pessoa **em até 6 minutos**. 3 levaram de 19 a 31 minutos. 1 mandou só mensagem automática. 1 não respondeu. 2 só responderam **na manhã seguinte**. |

**Etapa 2: reação à proposta (20 clínicas)**

| Situação | Qtd |
|---|---|
| Responderam à proposta | 7 |
| · Testou a demonstração e gostou | 1 |
| · Em conversa sobre como retoma pacientes hoje | 1 |
| · Recusaram sem explicar | 2 |
| · Recusou por valorizar o atendimento humanizado | 1 |
| · Já usa IA no atendimento | 1 |
| · Cautela por experiência ruim com automação, depois parou de responder | 1 |
| Pararam de responder logo depois que me identifiquei | 4 |
| Aguardando (contato em 27/10, à tarde) | 8 |
| Nunca responderam, nem como paciente | 1 |
| **Total** | **20** |

**Registros que ilustram os padrões**

- **Clínica A:** recusou explicando que valoriza o atendimento humanizado. Pediu para eu voltar a falar com a equipe no futuro.
- **Clínica B:** "temos uma IA que faz o CRC da clínica". Concorrência direta.
- **Clínica C:** a pessoa da recepção mostrou cautela por uma experiência anterior com automação que não funcionou.
- **Clínica D:** perguntada sobre os pacientes que somem depois do valor, respondeu que sim, têm um jeito de retomar. A conversa continua.
- **Clínica E:** aceitou ver a demonstração ("Sim claro") e testou o protótipo. Disse que gostou, achou interessante e muito útil para o agente atender quando a equipe não está online, sem perder vendas.

**Dado complementar (clínicas de harmonização, 27 e 28/10, fora da amostra principal):** uma clínica disse que "não gosta de deixar ninguém conversando com robô". Outra reclamou de ser testada como paciente e depois receber uma oferta. Uma terceira já atende com o assistente de IA da Meta.


---

## 7. Síntese dos feedbacks e padrões

1. **A demora fora do horário é real.** À noite, 5 de 6 clínicas só continuaram o atendimento no dia seguinte. É a evidência mais forte da rodada, porque foi observada e não declarada.
2. **Em horário comercial a situação varia muito.** Quase metade respondeu em minutos. A outra metade demorou de 19 minutos até o dia seguinte.
3. **As objeções não são sobre preço.** Elas falam de **toque humano** (2 casos somando harmonização), **concorrência** (clínicas que já usam IA) e **experiência ruim** com automação.
4. **O teste oculto custou confiança.** 4 clínicas pararam de responder logo depois que me identifiquei, e uma reclamou abertamente. Em 28/10 mudei a abordagem: passei a abrir com uma pergunta leve sobre atendimento à noite e no fim de semana, sem falar de IA no início.
5. **Quem testou enxergou o valor exatamente fora do horário.** O único feedback do protótipo bate com o padrão mais forte da etapa 1 e com o novo posicionamento.
6. **Ninguém afirmou perder pacientes.** A clínica que testou falou em "não perder vendas" como benefício, mas não relatou perdas que já tenha tido. A dor central da H1 continua sem confirmação direta.

---

## 8. Hipótese inicial x resultado

| Hipótese inicial | O que os dados mostraram |
|---|---|
| Clínicas demoram a atender no WhatsApp | **Confirmada na observação:** forte à noite, parcial em horário comercial. |
| Essa demora faz a clínica perder pacientes | **Sem confirmação:** nenhuma clínica relatou perda. Uma admitiu ter um processo para retomar quem some. |
| Clínicas vão se interessar por um agente de IA | **Fraca:** 1 de 7 que responderam testou a demonstração. 0 aceitaram pagar. |
| O agente será visto como útil | **Primeiro sinal positivo:** quem testou gostou e citou o atendimento fora do horário. Ainda é uma única avaliação. |
| O argumento forte é responder rápido, 24h | **Parcialmente contrariada:** as objeções foram toque humano, IA já existente e experiência ruim. |
| O mercado está livre | **Contrariada:** há clínicas que já usam IA no atendimento. |

---

## 9. Decisão final: **ajustar**

**Por que não perseverar:** H2 tem uma única avaliação e H3 não foi confirmada. Não há disposição de pagar.

**Por que não abandonar:** a dor do atendimento fora do horário foi observada na maioria das clínicas consultadas à noite, e a única clínica que testou o protótipo apontou esse mesmo valor. Há ainda uma conversa de descoberta em andamento.

**Por que não pivotar:** pivotar exige que a solução agrade de forma consistente e o problema seja só o pagamento. Uma avaliação positiva não basta para concluir isso.

**O que muda**

1. **Posicionamento:** de "agente que atende" para **"apoio à recepção fora do horário"**. O agente acolhe e agenda, e a equipe continua de manhã.
2. **Abordagem:** sem teste oculto. Conversa de descoberta primeiro, proposta depois. Já em prática desde 28/10.
3. **Foco:** clínicas **sem automação** e com atendimento humano só em horário comercial.
4. **Diferenciação:** responder à objeção de quem já teve experiência ruim (passagem fácil para humano, sem preço fechado, tom da clínica).

---

## 10. Próximo passo recomendado

**Rodada 2 (uma semana):**

- Mostrar a demonstração às clínicas que aceitarem e coletar nota e comentários (testa a H2).
- Conversar com 5 clínicas sem automação só sobre os pacientes que somem depois do valor, sem vender (testa a H1).
- Oferecer um piloto de 7 dias a quem confirmar a dor (testa a H3).

**Critérios da rodada 2, definidos antes de começar**

- H1 confirmada se pelo menos **3 de 5** relatam perder pacientes depois de perguntar o preço.
- H2 confirmada se pelo menos **3 de 5** dão nota 4 ou 5 à demonstração.
- H3 confirmada se pelo menos **2 de 5** aceitam o **piloto de 7 dias**.

Se H1 e H2 se confirmarem, construo o piloto no WhatsApp. Se nenhuma se confirmar, abandono o segmento.

---

## 11. Aprendizados

- **Observar vale mais do que perguntar.** O teste como paciente mostrou a demora com dados, sem depender da opinião de ninguém.
- **Mas observar escondido tem um custo.** A revelação depois do teste quebrou a confiança de parte das clínicas. O método precisa ser transparente.
- **Concorrência aparece cedo.** Mapear alternativas existentes deveria ter vindo antes da primeira abordagem.
- **Registrar tudo desde o primeiro contato** (data, horário, quem respondeu) é o que permite apresentar números que se sustentam.
- **Um resultado fraco, bem documentado, é mais útil do que um bom resultado sem prova.**

---

## 12. Uso de IA neste trabalho

**A IA foi usada para:**

- Claude: levantar ideias de problemas, estruturar hipóteses e critérios, redigir mensagens de abordagem, ler e organizar as conversas e a base do Notion, e redigir esta documentação.
- ElevenLabs: montar o agente de demonstração e narrar o vídeo com a minha voz.
- Apify: extrair a lista de clínicas do Google Maps.

**Eu fiz e decidi:** a escolha do problema e do segmento, todos os contatos com as clínicas, as anotações de cada conversa, a mudança de abordagem e a decisão final.

Nenhuma conclusão deste trabalho vem de respostas de modelo de IA. Todas vêm das conversas com as clínicas.

---

## Apêndice: protótipo de demonstração

**Agente "ImpulsAI · Demo Clínica Odontológica"**, montado no ElevenLabs para uma clínica **fictícia** ("Clínica Sorriso"). Conversa por voz e texto em português.

**O que ele faz**

- Cumprimenta, pergunta o nome e o que a pessoa procura.
- Explica os procedimentos de forma simples (o que é, como funciona, se dói), sem diagnóstico nem promessa de resultado.
- **Não informa preço fechado.** Explica que o valor depende do caso e é confirmado na avaliação.
- Propõe dois horários, confirma nome e telefone e fecha com um resumo do agendamento.
- **Fora do horário**, avisa que a equipe responde no próximo dia útil, mas já deixa a avaliação agendada.
- Diz que é uma assistente virtual se perguntarem, e passa para a equipe em caso de urgência, reclamação ou pedido de falar com uma pessoa.

**Limites:** roda no ElevenLabs, não no WhatsApp. Os horários, o endereço e os procedimentos são dados de exemplo. Foi avaliado por uma clínica até o fechamento (feedback positivo, sem nota numérica).
