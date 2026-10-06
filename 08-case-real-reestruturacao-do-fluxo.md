# Caso real: reestruturando um fluxo de demandas

> Diferente dos documentos anteriores, este não é um modelo. É o relato de algo que aconteceu, escrito sem dado de cliente, sem funcionalidade de produto e sem número absoluto de operação.

## Contexto

SaaS de gestão clínica, produto em operação, time pequeno. Quatro áreas conversam com desenvolvimento (Suporte, Customer Success, Treinamentos e Produto). Quando isso começou, não existia papel de produto na estrutura da empresa.

## Como era antes

Toda demanda ia direto para o repositório de desenvolvimento.

Qualquer pessoa, de qualquer área, abria a issue lá, no formato que achasse melhor. O desenvolvedor era a primeira pessoa a ler o pedido e também a primeira a descobrir que ele estava incompleto, duplicado, ou que descrevia um comportamento que o sistema já tinha.

O custo disso não aparece em relatório nenhum, porque não é uma falha visível. É tempo de desenvolvedor gasto fazendo triagem, e é demanda que espera semanas na fila para então voltar com "isso já existe".

## Primeira camada: Separar entrada de execução

Junto com um colega, criamos um segundo repositório, interno, e passamos a exigir que toda demanda nascesse ali.

A regra era simples, nada chega ao desenvolvimento sem passar por uma leitura antes.

Nessa fase a leitura era binária... Verificávamos se a demanda era válida e transferíamos, sem editar muito. Era pouco, mas resolveu o principal, o desenvolvedor deixou de ser o primeiro filtro.

O que essa camada não resolveu foi a demanda chegava válida, mas não chegava clara. Continuava sendo o pedido escrito por quem pediu, com a solução que a pessoa imaginou já embutida nele.

## Segunda camada: Refinamento como etapa obrigatória

Aqui eu assumi sozinho e é onde está o trabalho de verdade.

**Refinamento virou etapa, não favor.** Nenhuma demanda vai para desenvolvimento sem que o problema esteja separado da solução sugerida, sem comportamento atual e esperado escritos, e sem critério de aceite. 
Isso dá trabalho, leva tempo e é a parte que ninguém vê.

**Issue pai e filha.** A demanda original fica no repositório interno e nunca é editada: ela é o registro do que a pessoa pediu, nas palavras dela. O item de desenvolvimento é outro, escrito por mim, e aponta de volta para a origem. Assim é possível responder duas perguntas diferentes sem confundi-las: o que foi pedido, e o que foi construído.

**O quadro.** Montei o Project com views por área, régua de prioridade documentada e campos de origem da demanda, prioridade e versão de entrega. O estado de qualquer demanda passou a ser consultável sem ninguém precisar perguntar.

## A decisão mais difícil

Não foi técnica. Foi assumir que a maior parte do valor desse fluxo está em não construir.

Uma em cada quatro demandas que entram não vira código. Não porque fossem pedidos ruins, mas porque a resposta certa não era desenvolvimento: duplicata, comportamento que já existia, erro de processo, ou algo que se resolve com documentação ou treinamento.

É o número mais desconfortável de defender, porque parece improdutividade. É o contrário. Uma demanda que vira issue, entra na fila, espera semanas e só então revela que o problema era configuração custou duas coisas: o tempo do time e a paciência de quem pediu. Descobrir isso em dois dias devolve a solução para a pessoa.

## O que mudou

- O desenvolvedor parou de fazer triagem e voltou a fazer desenvolvimento
- A demanda tem rastro: dá para ir do que foi entregue até o pedido original, nas palavras de quem pediu
- Quase tudo que entra vem de fora de produto, o que significa que o fluxo serve às áreas e não a quem o desenhou
- O estado de qualquer demanda é consultável sem reunião

## O que eu faria diferente

**Teria medido antes.** Os números que eu uso hoje só existem porque fui apurar depois. Não tenho base de comparação do período anterior à primeira camada. Sei que melhorou, não consigo dizer quanto.

**Teria nomeado os estados com mais cuidado.** Um dos status do quadro significa "já passou por mim e está na minha fila", e é lido por muita gente como "está esperando desenvolvimento". Nome de status é contrato de comunicação, e eu tratei como etiqueta.

**Teria construído com as áreas, não para elas.** Desenhei o fluxo e depois expliquei. Funcionou, mas construir junto daria o mesmo resultado com menos explicação depois, e com menos dependência de uma pessoa só para sustentar o processo.

## O que ficou de método

- Separe o registro do pedido do registro do trabalho. Editar o pedido original apaga a informação de como a pessoa enxergava o problema.
- Refinamento sem etapa formal vira favor, e favor não escala.
- Estado visível vale mais que cerimônia de acompanhamento.
- A pergunta mais barata do fluxo é "isso precisa mesmo ser construído?", e ela só rende se for feita cedo.
