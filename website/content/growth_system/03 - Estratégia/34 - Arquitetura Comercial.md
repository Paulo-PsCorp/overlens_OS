---
title: Arquitetura Comercial
summary: "Documenta a migração da Overlens de uma operação dependente de lançamentos para aquisição e vendas contínuas: o que cada peça faz (aquisição, CRM, vendedores, follow-up, recuperação, WhatsApp, conteúdo, eventos, campanhas, produtos perpétuos, expansão e retenção), a diferença econômica entre campanha e sistema, o que já foi decidido nas páginas de Operação Comercial (Política Comercial, Responsabilidades Comerciais e Política de Mensagens) e o que ainda está pendente de decisão."
topics: [arquitetura comercial, vendas contínuas, crm, follow-up, retenção, expansão, lançamentos, operação]
keywords: [arquitetura comercial, aquisição contínua, vendas diárias, crm, vendedores, follow-up, recuperação de leads, whatsapp, conteúdo, eventos recorrentes, campanhas, produtos perpétuos, expansão de clientes, retenção, relacionamento de longo prazo, lançamento, sistema, em validação, política comercial, responsabilidades comerciais, política de mensagens, customer success, upgrade, renovação]
priority: high
ai_when_to_use: |
  Use quando o usuário perguntar como a Overlens vende, como funciona a operação comercial, o que muda com a migração de lançamentos para vendas contínuas, qual o papel de CRM, vendedores, follow-up, recuperação de leads ou WhatsApp, ou quando precisar saber o que já foi decidido e o que ainda está pendente na operação comercial.
related: [growth_system/03 - Estratégia/32 - Fluxos, growth_system/03 - Estratégia/33 - Growth Loop, growth_system/02 - Ofertas/23 - Ofertas, growth_system/04 - Operação Comercial/35 - Política Comercial, growth_system/04 - Operação Comercial/36 - Responsabilidades Comerciais, growth_system/04 - Operação Comercial/37 - Política de Mensagens, "business_doc/03 - Arquitetura/05 - Política de Instrutoria, Palestras e Ativos de Marca"]
---
# Arquitetura Comercial

## A Overlens está deixando de depender de lançamentos para operar com aquisição e vendas contínuas. Esta página documenta os conceitos que essa nova operação precisa comportar, e marca com clareza o que ainda não foi decidido.

A direção está tomada; o desenho operacional, não. Esta página existe para que ninguém confunda intenção com processo implantado. <dado q="B" />

O princípio que organiza tudo:

> **A Overlens deve operar como uma empresa baseada em sistemas, e não em campanhas.**

A definição de como a companhia captura valor pertence ao Business Document, em *Arquitetura de Receita*. Esta página trata do que pertence ao Growth System: **como as pessoas descobrem, consideram, compram, permanecem e expandem** dentro de uma operação que não desliga.

Parte do desenho operacional já existe na seção Operação Comercial: as regras de venda estão na [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial), quem responde por cada etapa está em [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais) e quem comunica, quando e por qual canal está na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens), ainda em minuta. Esta página aponta para elas onde houver resposta e mantém pendente o que nenhuma delas resolve. <dado q="B" nota="Política Comercial e Responsabilidades Comerciais com decisões aprovadas; Política de Mensagens em Minuta V1." />

## A diferença econômica entre campanha e sistema

A distinção não é de estilo. É de natureza econômica.

**Uma campanha concentra risco e recomeça.** O esforço se acumula em uma janela: preparação, evento comercial, pico, queda. O resultado depende de acertar aquela janela específica (audiência, oferta, timing, execução). Se ela falha, não há segunda chance dentro do ciclo, e o período inteiro fica comprometido. No ciclo seguinte, boa parte do trabalho é refeita do zero. O gasto de aquisição é pago de novo. A atenção é reconquistada de novo.

**Um sistema acumula.** Cada volta deixa algo que a próxima não precisa reconstruir: contatos que entraram e continuam na base, relacionamentos em andamento, conteúdo que segue atraindo, reputação que reduz o custo de convencer, clientes que compram de novo sem precisar ser reconquistados. O custo marginal de crescer tende a cair, e a receita deixa de depender de um único evento do calendário.

| | Campanha | Sistema |
| :---- | :---- | :---- |
| **Distribuição do risco** | Concentrado em janelas | Distribuído no tempo |
| **O que sobra ao fim do ciclo** | Resultado do período | Base, relacionamento e reputação |
| **Previsibilidade** | Baixa entre janelas | Construída com o tempo |
| **Custo de aquisição** | Pago de novo a cada ciclo | Parcialmente amortizado |
| **Dependência de pico** | Alta | Baixa |
| **Exigência operacional** | Intensidade concentrada | Consistência prolongada |

Duas ressalvas honestas. **Campanha não é erro**: lançamento é um mecanismo legítimo e a Overlens construiu sua operação com ele. E **sistema não é fácil**: ele troca intensidade concentrada por disciplina contínua, que é mais difícil de sustentar. A migração não elimina esforço, muda a forma do esforço.

## As peças da operação contínua

Cada peça abaixo descreve **o que faz e como se encaixa**. Quando uma regra já foi decidida ou proposta, a peça aponta a página dona dela, sem repetir o conteúdo. O resto (processo, cadência, script, ferramenta ou meta) segue sem decisão, e inventar seria documentar suposição como decisão.

### Aquisição contínua

Entrada permanente de pessoas novas no ecossistema, independentemente de haver evento comercial no calendário. É o que impede que a operação alterne entre abundância e escassez de contatos.

Encaixe: alimenta todas as demais peças. Sem entrada contínua, CRM e follow-up trabalham sobre uma base que só se renova em lançamentos.

Quais canais sustentam aquisição contínua, com que orçamento e sob qual responsabilidade? <dado q="E" />

### Vendas diárias

A venda deixa de ser evento e passa a ser rotina. Existe uma quantidade de conversas comerciais acontecendo todos os dias, não apenas nas semanas de abertura de carrinho.

Encaixe: transforma o fluxo de aquisição em receita de forma distribuída, reduzindo a dependência de picos.

Quais ofertas estão disponíveis para venda diária e quais permanecem em ciclos fechados? <dado q="E" />

### CRM

O sistema de registro e condução do relacionamento comercial: quem é cada pessoa, em que estado está, o que já aconteceu e o que deveria acontecer a seguir.

Encaixe: é a memória da operação. Sem ele, a continuidade depende de quem lembra, e uma operação contínua não pode depender de memória individual.

Quem registra o quê já tem desenho proposto: CS registra renovações e upgrades encaminhados; Comercial registra aceite, proposta e desfecho dos upgrades; origem, influência e fechamento ficam em campos distintos. Ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais). <dado q="C" nota="Registro mínimo e campos de CRM em proposta; só a separação entre origem, influência e fechamento está ratificada." />

Qual ferramenta, quais estágios e quais campos são obrigatórios, e como as funções viram perfis e permissões? <dado q="E" />

### Vendedores

Pessoas responsáveis por conduzir conversas comerciais, entender contexto, qualificar e acompanhar decisões, especialmente nas ofertas de ticket mais alto e ciclo mais longo, onde a decisão não se resolve sozinha em uma página.

Encaixe: é a camada humana entre o interesse e o compromisso. Sua qualidade define a experiência de compra tanto quanto o produto.

O escopo do setor está definido: o Comercial (B2C e B2B) responde por prospecção, qualificação, propostas, negociação e fechamento de novas vendas e dos upgrades encaminhados pelo CS, e centraliza os fechamentos de Overpass, Vanguarda, workshops, AI Build e implementações. Os limites de negociação estão na [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial). Ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais). <dado q="A" />

A remuneração de quem entrega (instrutoria) é separada da comissão comercial; ver [Política de Instrutoria, Palestras e Ativos de Marca](/business/03-arquitetura/05-politica-de-instrutoria-palestras-e-ativos-de-marca). <dado q="A" />

Quantas pessoas, com qual remuneração (OTE, variável, comissão interna) e com que critério de qualificação? Nenhum OTE ou percentual interno de comissão está aprovado. <dado q="E" />

### Follow-up

O acompanhamento de uma conversa iniciada e não concluída. A maior parte das decisões relevantes não acontece no primeiro contato. Sem acompanhamento, interesse legítimo se perde por ausência, não por recusa.

Encaixe: é o que converte o trabalho de aquisição já pago em resultado. É também a peça mais sensível ao tom: acompanhar é diferente de pressionar.

Os critérios gerais para decidir canal, momento, público e responsável de cada mensagem estão em minuta na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens). No upgrade, o Comercial assume em até 24 horas a oportunidade encaminhada pelo CS (ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais)). <dado q="B" nota="Política de Mensagens em Minuta V1; o prazo de 24 horas do upgrade está aprovado." />

Até quando se acompanha uma conversa comercial, com que frequência e com que limite? <dado q="E" />

### Recuperação de leads

Retomada de contatos que demonstraram interesse em algum momento e não avançaram. Uma base acumulada é um ativo; sem mecanismo de retomada, é apenas um arquivo.

Encaixe: aproveita o investimento de aquisição já realizado em ciclos anteriores: exatamente o tipo de acúmulo que a lógica de campanha desperdiça.

Para carrinho abandonado e inscritos ausentes em live, os critérios de elegibilidade e as verificações antes do disparo estão em minuta na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens); o intervalo ideal de abordagem ainda é hipótese em teste. <dado q="B" nota="Minuta V1, 10/10/2026." />

Que critérios definem um lead antigo como recuperável, com que frequência se retoma e com qual mensagem? <dado q="E" />

### WhatsApp

Canal de relacionamento direto e de alta proximidade. Concentra tanto conversas comerciais quanto relacionamento contínuo com quem já é da casa.

Encaixe: é onde boa parte do follow-up, da recuperação e do atendimento acontece. Por ser íntimo, é onde o tom da Overlens fica mais exposto.

Os usos do WhatsApp em grupo e individual, quem redige, envia e automatiza, e os critérios de frequência e abordagem estão na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens). Os disparos são registrados no ClickUp. <dado q="B" nota="Minuta V1, 10/10/2026." />

Que registro é feito no CRM e quais os limites numéricos de frequência? <dado q="E" />

### Conteúdo

Produção permanente que atrai, educa e sustenta reputação. Em uma operação contínua, o conteúdo deixa de ser aquecimento de lançamento e passa a ser infraestrutura de aquisição.

Encaixe: é a primeira etapa do ciclo de crescimento e o principal alimentador da aquisição contínua. Ver *Growth Loop*.

Que volume, formatos, canais e responsáveis sustentam essa operação? <dado q="E" />

### Eventos recorrentes

Encontros, imersões, hackathons e experiências que acontecem com regularidade. Funcionam simultaneamente como aquisição, ativação, comunidade e produção de projetos.

Encaixe: comprimem várias etapas do ciclo em um intervalo curto e criam pontos de contato previsíveis ao longo do ano, sem depender de um único evento comercial.

Quais eventos são recorrentes, em que periodicidade e com qual papel comercial? <dado q="E" />

### Campanhas

Intensificações deliberadas dentro de um sistema que já opera, não a operação inteira.

Encaixe: uma campanha sobre base, relacionamento e reputação acumulados é um pico; sem isso, é a única fonte de receita do período. A diferença é o que existe antes e depois dela.

Quantas campanhas por ano, com que ofertas e como convivem com a venda contínua? <dado q="E" />

### Produtos perpétuos

Ofertas disponíveis o ano inteiro, sem janela de abertura e fechamento. São a contrapartida de produto da lógica de venda contínua: não há venda diária sem algo que possa ser comprado todo dia.

Encaixe: sustentam a receita entre campanhas e permitem que a decisão aconteça no tempo da pessoa, não no tempo do calendário comercial.

A estrutura de preço vigente da Vanguarda, do Overpass individual e do Programa Empresarial Overpass está na [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial). <dado q="A" />

Quais ofertas se tornam perpétuas e em que formato? <dado q="E" />

### Expansão de clientes

Crescimento da relação com quem já é cliente: avanço para outra camada, novas frentes, mais profundidade.

Encaixe: é a fonte de receita mais barata da operação, porque dispensa aquisição. Depende de saber em que estado cada pessoa está, o que hoje ainda não é observável.

O upgrade Overpass → Vanguarda já tem regra e condutor: CS identifica a oportunidade e encaminha ao Comercial, que assume em até 24 horas, negocia e fecha, enquanto o CS conserva o relacionamento. O valor pago no Overpass (ou no Black Pass) pode virar crédito, respeitado o piso da nova venda. Ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais) e [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial). <dado q="A" />

Que movimentos de expansão existem além do upgrade e a partir de que sinal? <dado q="E" />

### Retenção

Permanência de quem já está dentro. Na camada contínua, permanência é receita; em todas as camadas, é condição para que projeto e evidência aconteçam.

Encaixe: uma operação contínua com retenção fraca é um funil disfarçado: enche na frente e vaza atrás, e o custo de aquisição nunca amortiza.

A renovação da Vanguarda é responsabilidade integral do CS, com preço-base congelado por cinco anos a partir da primeira compra enquanto não houver cancelamento. Pedidos de retenção, cancelamento, reembolso e compensação são centralizados pelo CS e decididos por Ruan ou Rafael, sem afastar obrigações legais. Ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais) e [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial). <dado q="A" />

Que sinais de permanência são acompanhados e o que se faz quando eles caem? <dado q="E" />

### Relacionamento de longo prazo

A camada que atravessa todas as outras: tratar cada pessoa como alguém que continua existindo depois da compra.

Encaixe: é o que diferencia um sistema comercial de uma máquina de conversão. Também é o que torna reputação e indicação possíveis: as entradas mais baratas do ciclo.

Depois da venda, o relacionamento com o cliente é do Customer Success, que recebe do Comercial o contexto da compra e conduz onboarding, acompanhamento e renovação. Ver [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais). <dado q="A" />

Como esse relacionamento se articula com comunidade e produto? <dado q="E" />

## Como as peças se encaixam

Uma leitura possível do encadeamento, sem assumir processo definido: <dado q="B" />

> **Conteúdo e eventos alimentam aquisição contínua · CRM registra e organiza · vendedores e follow-up conduzem · recuperação reaproveita o que não avançou · produtos perpétuos permitem que a compra aconteça a qualquer momento · retenção e expansão transformam cliente em relação · relacionamento de longo prazo devolve reputação e indicação para o começo do ciclo · campanhas intensificam pontualmente o que já está em operação.**

O teste de coerência: **se uma peça depende de uma janela específica para existir, ela pertence à lógica antiga.**

## O que muda em relação à operação por lançamento

| Dimensão | Operação por lançamento <dado q="D" /> | Operação contínua |
| :---- | :---- | :---- |
| **Ritmo** | Ciclos concentrados, com picos e vales | Operação permanente |
| **Origem da receita** | Eventos comerciais | Venda diária, recorrência e expansão |
| **Papel do conteúdo** | Aquecimento para uma janela | Infraestrutura de aquisição |
| **Papel da base de contatos** | Insumo do próximo lançamento | Ativo permanente com relacionamento ativo |
| **Papel do vendedor** | Concentrado na janela | Função contínua |
| **Papel do CRM** | Opcional | Estrutural |
| **Relação com o cliente** | Termina na compra | Continua na permanência e na expansão |
| **Principal risco** | Uma janela ruim compromete o período | Inconsistência prolongada corrói o sistema |

## Histórico: a operação por lançamento

O modelo anterior, preservado como registro do que foi construído e praticado. <dado q="D" />

A Overlens operou com GTM estruturado por estágios e concentrado em eventos comerciais: **Atlas** com Product Led Growth em 1 estágio; **Overpass** com Product Led Growth em 2 estágios; **Vanguarda** com modelo de eficiência em 2 estágios. Lotes, datas de abertura e janelas de inscrição faziam parte da mecânica, e o esforço de aquisição se concentrava nas semanas anteriores a cada abertura.

**O que esse modelo acertava:** concentração de energia, clareza de calendário, senso de evento e capacidade de gerar receita significativa em pouco tempo.

**O que não sustentava:** receita dependente de janelas, esforço refeito a cada ciclo, relacionamento que esfriava entre lançamentos e base de contatos subaproveitada.

Esse modelo **não é abandonado**: campanhas seguem sendo um mecanismo válido. O que muda é o estatuto: deixam de ser a operação e passam a ser parte dela.

## O que precisa ser decidido

Consolidação das decisões ausentes. Nenhuma deve ser preenchida por suposição. Onde já existe resposta parcial, o item aponta a página dona e diz o que falta.

1. **Quais ofertas se tornam perpétuas** e quais permanecem em ciclos fechados. A estrutura de preço vigente já está na [Política Comercial](/growth/04-operacao-comercial/35-politica-comercial).
2. **Qual ferramenta de CRM** e quais estágios do relacionamento são registrados nela. Quem registra o quê está proposto em [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais); faltam procedimento, campos obrigatórios, perfis e permissões.
3. **Estrutura do time comercial:** escopo por setor e ofertas sob responsabilidade já definidos em [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais); faltam quantidade de pessoas, remuneração (OTE, variável, comissões internas) e metas.
4. **Política de follow-up:** momento, canal, responsável e limite. Os critérios gerais de canal, momento e responsável estão em minuta na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens); faltam aprovação e limites do follow-up comercial.
5. **Critérios de recuperação de leads:** o que caracteriza um contato recuperável e com que frequência se retoma. Carrinho abandonado e inscritos ausentes já têm critérios em minuta na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens); leads antigos seguem sem critério.
6. **Uso do WhatsApp:** critérios de canal e responsáveis propostos na [Política de Mensagens](/growth/04-operacao-comercial/37-politica-de-mensagens) (Minuta V1); faltam aprovação final, registro no CRM e limites numéricos de frequência.
7. **Operação de conteúdo:** volume, formatos, canais e responsáveis.
8. **Calendário de eventos recorrentes** e o papel comercial de cada um.
9. **Convivência entre campanhas e venda contínua** ao longo do ano.
10. **Sinais de retenção e de expansão** que a operação acompanha, e o que se faz quando eles caem. Os responsáveis por renovação, upgrade e retenção já estão definidos em [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais).
11. **Articulação do relacionamento pós-venda com comunidade e produto.** O responsável (Customer Success) já está definido em [Responsabilidades Comerciais](/growth/04-operacao-comercial/36-responsabilidades-comerciais).
12. **Indicadores da operação comercial.** Nenhuma meta, taxa ou número está definido, e nenhum deve ser inferido de documentos anteriores sem revalidação.
