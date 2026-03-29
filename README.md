# 📋 Checklist eMAG
> Projeto de conclusão do curso de Ciência da Computação | Universidade Federal Fluminense

---

## 📌 Sumário

* [❓ Sobre o eMAG](#-sobre-o-emag)
* [🎯 Motivação do checklist](#-motivação-do-checklist)
* [🚧 Limitações do eMAG e do checklist](#-limitações-do-emag-e-do-checklist)
* [💡 Funcionalidades](#-funcionalidades)

---

## ❓ Sobre o eMAG

O **eMAG (Modelo de Acessibilidade em Governo Eletrônico)** é um modelo brasileiro voltado a orientar a construção e avaliação de conteúdos e interfaces digitais acessíveis, com foco especial no contexto de serviços e portais. Ele consolida recomendações práticas para reduzir barreiras de uso para pessoas com deficiência e outros perfis (por exemplo, pessoas com limitações temporárias, baixo letramento digital ou uso em dispositivos e ambientes restritivos).

Apesar de criado com o compromisso de nortear a adaptação e o desenvolvimento de conteúdos digitais do Governo Federal, o eMAG é fortemente relacionado às diretrizes internacionais do **WCAG (*Web Content Accessibility Guidelines*)**. Por isso, ele também serve como um guia geral aplicável à realidade brasileira e às necessidades de serviços digitais em diferentes contextos e esferas. Nesta aplicação, os itens do checklist são organizados com base no [eMAG v3.1](https://emag.governoeletronico.gov.br/), e, quando pertinente, incluem também referências associadas ao [WCAG 2.2](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/) e a outras fontes de prestígio para facilitar a rastreabilidade e o estudo.

---

## 🎯 Motivação do checklist

Nos últimos tempos, serviços e informações digitais estão cada vez mais presentes no dia a dia. Em diversas esferas da sociedade, muitas atividades e processos que antes eram físicos passaram a acontecer na Web. Além disso, novas automações foram criadas para facilitar nossas vidas. Nesse contexto, é fácil constatar que, se uma aplicação digital não é acessível, então parte das pessoas ficam, na prática, marginalizadas do resto da população.

Pessoas com deficiência ainda enfrentam barreiras de participação em vários cenários, e isso também acontece no ambiente digital. No Brasil, a inclusão e a acessibilidade desse público são respaldadas por normas e políticas públicas no âmbito da Constituição Federal e de legislações como a Lei Brasileira de Inclusão, o que reforça a noção de que acessibilidade é um requisito necessário para o exercício da cidadania.

Por outro lado, a acessibilidade não se limita somente a pessoas com deficiência. Ela também beneficia qualquer indivíduo em situações reais de uso: limitações temporárias, envelhecimento, baixa familiaridade com tecnologia, acesso por celular, conexão instável, ambientes com ruído ou baixa iluminação, entre outras condições.

Por isso, as recomendações de acessibilidade na Web evoluem continuamente para acompanhar mudanças na tecnologia e nos padrões de interação. O WCAG é uma das principais referências internacionais nessa conjuntura e serve de base para várias iniciativas ao redor do mundo.

Diversos governos e instituições governamentais mundo afora adaptam essas diretrizes para os contextos e necessidades específicos de cada região. No Brasil, esse papel é exercido pelo eMAG. O problema é que a última versão revisada do eMAG (v3.1, de abril de 2014) já é antiga considerando o intenso e constante desenvolvimento da tecnologia e da internet. Sendo assim, é natural que suas recomendações possam ter sofrido com o processo de defasagem, ambiguidade ou baixo alinhamento em relação a aplicações modernas.

Com isso em mente, esta aplicação web foi construída como parte de um **projeto de TCC**, com a meta de estabelecer uma proposta prática de **modernização do eMAG**, estruturada em formato de checklist. A premissa central consistiu em adaptar as recomendações originais, definir critérios de verificação e incluir novas referências quando necessário, conforme uma análise de defasagem previamente realizada. O objetivo foi trazer o eMAG para um contexto mais moderno frente às mudanças propagadas nas tecnlogias da informação e nas orientações de acessibilidade digital.

A **análise de defasagem** das recomendações do eMAG está disponível no [repositório do GitHub](https://github.com/LuizWillner/checklist-emag/blob/main/revisao-do-emag.md). Para cada uma das recomendações, foi feita uma discussão embasando a relevância atual da orientação, expondo os eventuais pontos de defasagem e explicando as mudanças feitas no item análogo do checklist.

---

## 🚧 Limitações do eMAG e do checklist

Apesar do eMAG ser um ótimo ponto de partida, ele foi pensado historicamente com forte aderência ao contexto de portais e serviços governamentais e a padrões mais "clássicos" de conteúdo na Web. Esse fator somado a outros traz algumas limitações práticas para ele, e consequentemente para o checklist:

* **Cobertura e interpretação:**
  alguns itens exigem julgamento técnico e contextual. Numa internet que dispõe de arquiteturas e aplicações cada vez mais complexas e diversas (SPAs, componentes dinâmicos, estados ricos de interface), pode ser necessário complementar a análise de acessibilidade com outros critérios, práticas e testes adicionais.

* **Conformidade ao checklist não garante total acessibilidade:**
  marcar os itens como "conformes" no checklist não necessariamente sustenta plena acessibilidade da aplicação inspecionada. Não só pela gama variada de sistemas que podem não ser totalmente contemplados pelos itens do checklist, mas também pela constante evolução da tecnologia e das diretrizes de acessibilidade. Por isso, uma inspeção realizada com o checklist não garante invariavelmente conformidade legal ou normativa. A ferramenta serve como apoio, e não dispensa a aplicação de outros instrumentos, técnicas e análises na realização de uma auditoria completa e robusta. A acessibilidade real depende de uma série de variáveis, como comportamento efetivo, tecnologias assistivas, navegação por teclado, leitores de tela, contraste, conteúdo, entre outras.

* **Evidências variam:**
  certos critérios podem depender mais do que uma simples inspeção visual da página ou do código fonte e requerir o uso de outras técnicas, como testes com leitores de tela. Algumas ferramentas de análise automática de acessibilidade podem ser úteis para fornecer insights iniciais.

* **Referências são apoio:**
  links e referências aqui estabelecidos ajudam a entender e se aprofundar nos tópicos, mas podem mudar ao longo do tempo com atualizações do conteúdo, reorganização de páginas, versões, entre outros.

---

## 💡 Funcionalidades

O checklist foi desenhado para você conduzir uma inspeção de forma incremental: marcar itens, registrar observações, consultar critérios e referências, abrir exemplos práticos e acompanhar o progresso.

Além disso, há três "níveis" disponíveis de salvamento de progresso:

1. Salvamento local no navegador
2. Salvamento local em arquivo (relatório)
3. Salvamento no servidor (código de recuperação)

---

### 🧰 Barra de ferramentas

| Ação                   | Descrição                                                     |
| ---------------------- | ------------------------------------------------------------- |
| 🔄 **Gerar código**    | Salva o progresso no servidor e gera um código de recuperação |
| 🔄 **Sincronizar**     | Atualiza o progresso salvo no servidor                        |
| 📋 **Código (copiar)** | Permite copiar o código vinculado                             |
| ⬇️ **Recuperar**       | Carrega progresso salvo                                       |
| 📤 **Exportar**        | Gera relatório (.xlsx ou .ods)                                |
| 📥 **Importar**        | Importa relatório e sobrescreve o progresso                   |
| 🧹 **Limpar**          | Reinicia o checklist                                          |

---

### 💾 Salvamento automático

A aplicação conta com um mecanismo de salvamento automático, em que cada alteração feita na inspeção é **salva localmente** no navegador.

---

### ✅ Marcando o checklist

| Estado          | Descrição                                                           |
| --------------- | ------------------------------------------------------------------- |
| Não marcado     | O item não foi marcado                                              |
| ✔️ Conforme     | o requisito foi atendido (com base na evidência que você verificou) |
| ❌ Não conforme  | o requisito não foi atendido                                        |
| ➖ Não se aplica | o requisito não se aplica                                           |

---

### 🔍 Detalhamento dos itens

* **Descrição do item:** apresenta o enunciado e o contexto
* **Critérios de verificação:** perguntas objetivas (sim/não)
* **Referências:** links organizados por origem
* **Notas da inspeção:** registro de evidências
* **Exemplos:** casos práticos com boas e más práticas

---

### 📊 Barra de progresso

A barra de progresso resume visualmente a inspeção com percentuais e contagens dos **itens conformes e não conformes**.

Itens marcados como **"Não se aplica" são descontados do total**, evitando distorções.

---

## 📎 Recursos adicionais

* 📄 [Análise de defasagem do eMAG](https://github.com/LuizWillner/checklist-emag/blob/main/revisao-do-emag.md)

---
