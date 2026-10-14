---
paths:
  - "[PAGINA]*"
  - "[PESQUISA]*"
---

# Padrão para Páginas da Base de Conhecimento

> **Leia antes:** `.claude/rules/tese-atual.md`, fonte normativa sobre quem é o público, o que a Overlens é, o papel da IA e o vocabulário atual. Em conflito, aquela regra prevalece sobre qualquer documento da base.

## Regras de Escrita

Toda página criada para a base de conhecimento da Overlens DEVE:

1. Começar com H1 (título limpo) seguido de H2 (frase evocativa)
2. Usar português brasileiro acessível, sem jargão, sem gíria, sem formalidade excessiva
3. Respeitar as 4 virtudes: Científica, Profunda, Provocativa, Inspiradora
4. Incluir os guardrails éticos: sem guru, sem dogma, sem culpabilização
5. Seguir a **regra de público** e o **vocabulário atual** (abaixo)
6. Seguir metáforas do universo Overlens: fogo controlado, prisma, portal, micélio
7. **Classificar certeza** quando a afirmação for estratégica, com a tag `dado` fechando o bloco, como uma nota, por exemplo `... e quer transformá-la em realidade. <dado q="A" />` (ver "Classificação de Certeza", abaixo)
8. EVITAR: lâmpada clichê, varinha mágica, forja, FOMO, hustle porn, promessas vazias

## Regra de Público, ELIMINATÓRIA

O público da Overlens é o **empreendedor**: quem tem uma ideia, ambição ou visão de futuro e quer transformá-la em realidade.

**O que define o público é o estado, não a profissão.** Esse empreendedor **pode ou não** ser designer, engenheiro, arquiteto, artista, inventor, maker ou pesquisador, e pode ser também um empreendedor de qualquer outra origem, inclusive sem formação específica.

**Proibido:**
- Chamar o público de "designers", "criativos" ou "profissionais criativos" como rótulo, porque design é uma das disciplinas que a Overlens ensina, não quem nos procura
- Definir o público por profissão, formação, cargo ou senioridade
- Usar "Empreendedor Nexialista" como nome do público

**Permitido:**
- "Empreendedor" como substantivo do público
- Profissões como **exemplos de origem**: "pode vir da engenharia, da arquitetura, da arte, do design ou de nenhuma dessas origens"
- Profissões dentro da **estrutura dinâmica de posicionamento**: "a escola de negócios dos criadores / dos artistas / dos engenheiros / dos designers"

> *"Nosso público são designers"* → proibido. *"A escola de negócios dos designers"*, como variação da expressão de posicionamento → permitido.

## Vocabulário

**Termos oficiais:** Overlens · **Atom** (membro da comunidade) · Nexialismo (capacidade, não rótulo de público) · Atom Praxis · Lente · Sistema Vivo · Capital Simbólico · projeto · evidência · realização

**Os quatro modos** são formas de agir, aprender, pensar e criar. **Não** são estágios sequenciais de maturidade, **não** hierarquia de senioridade:

> **Operante executa · Convergente conecta · Emergente cria · Nexialista orquestra**

**Obsoleto, não usar:**
- "Inconscientes" como perfil
- Os quatro modos descritos como "distância entre a ideia e a realidade"
- "Empreendedor Nexialista" como nome do público
- "átomo" como unidade de conteúdo
- Overlens como "escola de IA", ou "ensinar IA" como finalidade
- Overpass como "biblioteca", "assinatura de cursos" ou "Netflix de cursos"
- Vanguarda como "curso premium" ou apenas "mentoria"
- Cursos, assinatura ou lançamentos como única forma de monetização

## Termos Proibidos em Páginas

- "destrave", "acenda", "forje"
- "vagas limitadas", "última chance"
- "você pode tudo", "sem limites"
- "guru", "mestre iluminado"
- promessas de enriquecimento, faturamento ou "liberdade financeira"
- "escale seu negócio", "6 em 7", glamourização de rotina extrema, tom de startup bro
- qualquer promessa de resultado garantido
- **travessão (— ou –)**: proibido em toda a base. Use dois pontos, vírgula, ponto ou parênteses

### Vícios de escrita a evitar

Vêm do [Guia Rápido de Escrita](../../website/content/estudio_criativo/07%20-%20Guia%20de%20Escrita/01%20Guia%20Rápido%20de%20Escrita.md) (`website/content/estudio_criativo/07 - Guia de Escrita/01 Guia Rápido de Escrita.md`, minuta V1), que é a referência completa. Não são proibidos isoladamente: só aparecem quando fizerem sentido no contexto, e nunca como cadência ou assinatura de estilo.

- fórmulas "não é X, é Y" e "mais do que X", tríades artificiais, contrastes forçados, perguntas retóricas respondidas na frase seguinte e sequências de frases curtas que não avançam a ideia
- vocabulário vazio: "em um mundo cada vez mais", "no cenário atual", "jornada transformadora", "desbloquear potencial", "elevar a outro nível", "insights valiosos", "mergulhar profundamente", "sem precedentes"; "incrível", "poderoso" e "revolucionário" sem demonstração
- abstração sem significado, falsa profundidade, generalização sem prova, repetição da tese, falso equilíbrio
- entusiasmo automático, motivação genérica, intimidade fabricada, tom professoral, emojis decorativos
- negrito em palavras comuns, subtítulo a cada dois parágrafos, lista para qualquer raciocínio, cadência sempre simétrica

Revise com as três perguntas do guia: poderia ser texto de qualquer empresa? Há substância concreta? Alguém escreveria assim nesse canal?

## Classificação de Certeza

Toda afirmação estratégica nasce marcada. A marcação não é escrita por extenso: é uma **nota que fecha o bloco** e que o site renderiza como uma bolinha de qualidade.

```
O público da Overlens é o empreendedor. <dado q="A" />
Duas turmas já rodaram no formato novo. <dado q="B" nota="Direção testada em duas turmas." />
A categoria é escola de negócios, criação e realização. <dado q="A" fonte="TRU/changes.md" />
"A escola de negócios dos criadores" é a expressão em exploração. <dado q="C" nota="Candidato mais forte." fonte="https://exemplo.com/pesquisa" />
```

Atributos: `q` é obrigatório e vai de `A` a `E`; `nota` é opcional e leva uma frase curta de qualificação; `fonte` é opcional e só aparece quando o documento **declara** de onde a informação veio.

| Bolinha | Significa | Quando usar |
| :---- | :---- | :---- |
| **A** | DEFINIDO | Decisão tomada e atualmente válida |
| **B** | EM VALIDAÇÃO | Direção em teste, com evidência parcial |
| **C** | HIPÓTESE | Possibilidade ainda não validada |
| **D** | HISTÓRICO | Já foi verdadeiro; não representa a direção atual |
| **E** | PENDENTE | Precisa existir e ainda não existe |

No site, cada letra aparece como um ponto colorido com tooltip: a bolinha mostra a letra, o tooltip abre o significado e a nota. Quando a afirmação tem fonte declarada, um segundo ponto marcado **F** aparece ao lado e leva à origem.

Regras de uso:

- A tag **fecha o bloco que classifica**, como uma nota: vem depois da pontuação final, separada por um espaço. Fim do parágrafo, fim do item de lista, fim da última linha do blockquote, fim do texto da célula da tabela. Nunca fica sozinha numa linha separada do texto que classifica.
- **Nunca invente fonte.** A ausência de fonte é informação verdadeira sobre a base.
- Na dúvida entre `A` e `B`, escolher **`B`**.

## Regra de Histórico

Informação historicamente verdadeira **não é apagada**. Quando um posicionamento, produto ou conceito for substituído, mova o registro para uma seção de **Histórico / Posicionamentos anteriores / Evolução** e feche o bloco com `<dado q="D" />`.

O erro a evitar não é preservar o passado: é permitir que ele seja lido como a definição atual da companhia.

## Regra de Imagens

- NUNCA coloque uma imagem como primeiro elemento após o banner (H1 + H2)
- Sempre inclua pelo menos alguns parágrafos de texto antes da primeira imagem
- O leitor precisa de contexto textual antes de ver uma imagem

## Regra de Arquivos

- A fonte canônica é `website/content/<sistema>/...`, que inclui **frontmatter** (title, summary, topics, keywords, priority, ai_when_to_use, related)
- `TRU/<sistema>/...` é o mesmo corpo **sem frontmatter**
- Ao editar uma página, atualize os dois e revise o frontmatter se termos do vocabulário mudaram
- Páginas novas: `NN - Nome da Página.md` dentro da seção numerada

## Estrutura Mínima

```
# Título
## Frase de abertura
Parágrafos introdutórios...
## Seção 1
...
## Seção 2
...
```
