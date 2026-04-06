# Proposta de revisão do eMAG para o Checklist eMAG
> Documentação estruturada da análise das recomendações do Modelo de Acessibilidade em Governo Eletrônico (eMAG) v3.1 que serviu como suporte para a aplicação web de checklist de acessibilidade baseada no eMAG.

## Motivação

Nos últimos tempos, serviços e informações digitais estão cada vez mais presentes no dia a dia. Em diversas esferas da sociedade, muitas atividades e processos que antes eram físicos passaram a acontecer na Web. Além disso, novas automações foram criadas para facilitar nossas vidas. Nesse contexto, é fácil constatar que, se uma aplicação digital não é acessível, então parte das pessoas ficam, na prática, marginalizadas do resto da população.

Pessoas com deficiência ainda enfrentam barreiras de participação em vários cenários, e isso também acontece no ambiente digital. No Brasil, a inclusão e a acessibilidade desse público são respaldadas por normas e políticas públicas no âmbito da Constituição Federal e de legislações como a Lei Brasileira de Inclusão, o que reforça a noção de que acessibilidade é um requisito necessário para o exercício da cidadania.

Por outro lado, a acessibilidade não se limita somente a pessoas com deficiência. Ela também beneficia qualquer indivíduo em situações reais de uso: limitações temporárias, envelhecimento, baixa familiaridade com tecnologia, acesso por celular, conexão instável, ambientes com ruído ou baixa iluminação, entre outras condições.

Por isso, as recomendações de acessibilidade na Web evoluem continuamente para acompanhar mudanças na tecnologia e nos padrões de interação. O WCAG é uma das principais referências internacionais nessa conjuntura e serve de base para várias iniciativas ao redor do mundo.

Diversos governos e instituições governamentais mundo afora adaptam essas diretrizes para os contextos e necessidades específicos de cada região. No Brasil, esse papel é exercido pelo eMAG. O problema é que a última versão revisada do eMAG (v3.1, de abril de 2014) já é antiga considerando o intenso e constante desenvolvimento da tecnologia e da internet. Sendo assim, é natural que suas recomendações possam ter sofrido com o processo de defasagem, ambiguidade ou baixo alinhamento em relação a aplicações modernas.

Com isso em mente, uma aplicação web foi construída como parte de um **projeto de TCC**, com a meta de estabelecer uma proposta prática de **modernização do eMAG**, estruturada em formato de checklist. A premissa central consistiu em adaptar as recomendações originais, definir critérios de verificação e incluir novas referências quando necessário, conforme a seguinte análise de defasagem. O objetivo foi trazer o eMAG para um contexto mais moderno frente às mudanças propagadas nas tecnlogias da informação e nas orientações de acessibilidade digital.

## Metodologia da análise

No intuito de se compreender melhor o estado do eMAG perante às práticas e recomendações de acessibilidade web modernas, cada recomendação original foi classificada qualitativamente de acordo com **quatro níveis de defasagem**. Essa classificação foi orientada, de maneira geral, pelos seguintes critérios estabelecidos para cada nível:

- **Nível nulo**: A recomendação do eMAG está bem adequada e não possui nada que indique alguma orientação com defasagem significativa. Em outras palavras, elas podem ser seguidas como critérios adequados de acessibilidade sem maiores modificações.

- **Nível leve**: Há na recomendação do eMAG algum ponto que estabelece uma orientação de uma maneira antiga ou antiquada, mas que não está proprimante errada, e sim, que existem alternativas mais modernas que podem ser empregadas. Portanto, há a presença de fatores mais antigos, que eventualmente até podem trazer alguma leve melhora técnica caso fossem modernizados, mas que não há impacto relevante direto na acessibilidade ou em conformidade com padrões de linguagem.

- **Nível moderado**: Há na recomendação do eMAG um orientação antiquada que pode potencialmente introduzir algum problema para a aplicação, mesmo que não crítico, havendo uma alternativa objetivamente melhor que seria adequada ser empregada no lugar. Essa orientação original pode até não estar todo errada, mas as alternativas modernas poderiam minimizar as chances de impactos negativos ocorrerem.

- **Nível crítico**: Uma parte da recomendação do eMAG ou ela por completo orienta algo de uma maneira equivocada, em que o emprego desse método hoje induz a algum erro técnico mais grave, como não conformidade com o padrão sintático ou semântico de alguma linguagem ou a um prejuízo direto e relevante de acessibilidade. Portanto, a orientação estaria bastante ultrapassada, e alternativas mais adequadas deveriam ser empregadas no lugar.

Mesmo com esses critérios definidos, é necessário ainda compreender que a classificação de defasagem de uma recomendação em um nível maior ou menor pode ainda em muitos casos depender de um viés bastante interpretativo. Por exemplo, há uma série de recomendações que não possuíam defasagem aparente em seu texto em si, mas que os exemplos fornecidos relativos a ela muitas vezes demonstravam pontos antiquados. Classificar o nível de defasagem dessas recomendações dependia frequentemente da interpretação de se o exemplo era estabelecido como um modelo a ser seguido ou somente como uma simplificação proposital para melhorar a didática e ilustrar alguma ideia. No primeiro caso, a defasagem do exemplo tende a elevar a classificação, enquanto no segundo o nível tende a ser mais baixo. De todo modo, o ponto é que identificar em qual dos casos o exemplo se encontra pode ser algo subjetivo e requerir uma extrapolação da intenção original dos autores do documento. Esse é somente um dos casos que demonstram como a classificação é fundamentada a partir de uma análise qualitativa da recomendação original.

A seguir, segue uma tabela que resume as classificações feitas na análise para as recomendações por categoria.

## Resumo da análise

|                              | Nível Nulo | Nível Leve | Nível Moderado | Nível Crítico |
| ---------------------------- | ---------- | ---------- | -------------- | ------------- |
| 1. Marcação                  | 3          | 3          | 2              | 1             |
| 2. Comportamento (DOM)       | 6          | 0          | 0              | 1             |
| 3. Conteúdo/Informação       | 6          | 3          | 1              | 2             |
| 4. Apresentação/Design       | 1          | 2          | 1              | 0             |
| 5. Multimídia                | 3          | 0          | 2              | 0             |
| 6. Formulários               | 2          | 2          | 3              | 1             |
| Padronização no Gov. Federal | -          | -          | -              | -             |
| **TOTAL**                    | **21**     | **10**     | **9**          | **5**         |

## Análise

Para cada uma das recomendações, foi feita uma discussão embasando a relevância atual da orientação, expondo os eventuais pontos de defasagem e explicando as mudanças feitas no item análogo do checklist.

Para manter a estrutura do eMAG, a análise de cada item está separada dentre as categorias das recomendações:

1) [Marcação](#1-marcação)
2) [Comportamento (DOM)](#2-comportamento-dom)
3) [Conteúdo/Informação](#3-conteúdoinformação)
4) [Apresentação/Design](#4-apresentaçãodesign)
5) [Multimídia](#5-multimídia)
6) [Formulários](#6-formulários)
7) [Elementos padronizados de acessibilidade digital no Governo Federal](#elementos-padronizados-de-acessibilidade-digital-no-governo-federal)

----------------------------------------------------------------------------

### 1 Marcação

#### 1.1 Respeitar os Padrões Web

----------------------------------------------------------------------------

#### 1.2 Organizar o código HTML de forma lógica e semântica

----------------------------------------------------------------------------

#### 1.3 Utilizar corretamente os níveis de cabeçalho

----------------------------------------------------------------------------

#### 1.4 Ordenar de forma lógica e intuitiva a leitura e tabulação

**Defasagem do eMAG: nível nulo.**

A recomendação permanece consistente com orientações de acessibilidade atuais. Porém, algumas adaptações foram feitas, no intuito de clarificar e contextualizar mais a interpretação dos seguintes aspectos do texto original:

- No quarto critério de verificação, foi incorporado mais detalhes sobre o uso do atributo `tabindex` para evitar valores maiores que 0 atribuídos, e tomar cuidado caso esses valores sejam utilizados. Em outras palavras, seu uso não foi proibido (afinal, o eMAG e o WCAG não o proíbem), apenas foi melhor explicado o que seria usar o `tabindex` com cuidado, conforme explicado pela [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Global_attributes/tabindex). Essa referência sobre o uso de `tabindex`, que ainda justifica a orientação de evitar os valores maiores que 0, também foi adicionada.

- O 3º critério de recomendação, sobre colocar no código-fonte o menu depois do conteúdo principal, foi removido. Isso porque o termo "é recomendável" antes de mencionar isso no eMAG sugere isso como algo opcional, apesar de haver uma justificativa plausível para isso. Uma discussão sobre essa questão foi movida para o exemplo de aplicação.

- Além disso, o exemplo de aplicação do eMAG foi modernizado para usar elementos HTML semanticamente mais adequados.

----------------------------------------------------------------------------

#### 1.5 Fornecer âncoras para ir direto a um bloco de conteúdo

**Defasagem do eMAG: nível crítico.**

Apesar da ideia central da orientação ser válida, o eMAG está bem defasado em relação a essa recomendação, conforme discutido a seguir.

Em primeiro lugar, a recomendação do uso do atributo `name` junto ao `id` no elemento `<a>` não é válido no padrão do HTML. Isso porque o atributo `name` é obsoleto nesse elemento e seu uso é desencorajado, conforme a [especificação do HTML Living Standard](https://html.spec.whatwg.org/multipage/obsolete.html#obsolete-but-conforming-features).

Em segundo lugar, o uso do elemento `<a>` como pontos alvo de ancoragem também é prática defasada. Tanto o [WCAG na técnica G23](https://www.w3.org/WAI/WCAG22/Techniques/general/G123#:~:text=Example%204%3A%20HTML%20page%20with%20several%20blocks%20of%20navigation) quanto o [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/a#skip_links) sugerem exemplos em que o link aponta diretamente para um outro elemento com o id especificado, e não para uma outra âncora `<a>`.

Além disso, o uso do atributo `accesskey` para atalhos de teclado é potencialmente problemático. No eMAG, ele é mencionado apenas como sugestão, mas há fontes atuais que até mesmo o desencoraja por ser capaz de conflitar com outros atalhos do sistema operacional e de tecnologias assistivas, como dito no [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/accesskey#accessibility_concerns). O WCAG, principal referência de acessibilidade, nada fala sobre o uso ou não do `accesskey`.

Portanto, as seguintes refatorações foram feitas:

- Desconsiderar uso do atributo `name` no elemento `<a>`, pois ele não é mais suportado nesse elemento. O exemplo em que `name` e `id` são usados serã colocado como uma má prática a ser evitada.

- Desconsiderar o uso do elemento `<a>` como pontos alvo de ancoragem (e portanto, também as técnicas citadas para esconder esses pontos de ancoragem). Seu uso só aparecerá na má prática usada para ilustrar o uso de `name` e `id`.

- A sugestão de uso do `accesskey` feita no eMAG não foi portada para o checklist, por se tratar de apenas uma sugestão e que ainda por cima é capaz de trazer problemas de acessibilidade, a depender da implementação.

----------------------------------------------------------------------------

#### 1.6 Não utilizar tabelas para diagramação

----------------------------------------------------------------------------

#### 1.7 Separar links adjacentes

----------------------------------------------------------------------------

#### 1.8 Dividir as áreas de informação

----------------------------------------------------------------------------

#### 1.9 Não abrir novas instâncias sem a solicitação do usuário

----------------------------------------------------------------------------

### 2 Comportamento (DOM)

#### 2.1 Disponibilizar todas as funções da página via teclado

----------------------------------------------------------------------------

#### 2.2 Garantir que os objetos programáveis sejam acessíveis

----------------------------------------------------------------------------

#### 2.3 Não criar páginas com atualização automática periódica

----------------------------------------------------------------------------

#### 2.4 Não utilizar redirecionamento automático de páginas

----------------------------------------------------------------------------

#### 2.5 Fornecer alternativa para modificar limite de tempo

----------------------------------------------------------------------------

#### 2.6 Não incluir situações com intermitência de tela

----------------------------------------------------------------------------

#### 2.7 Assegurar o controle do usuário sobre as alterações temporais do conteúdo

**Defasagem do eMAG: nível nulo**

No WCAG 2.0, o [Critério de Sucesso 2.2.2: Colocar em pausa, parar e ocultar](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-pause.html), ao qual essa recomendação referencia, é um pouco mais flexível, sobretudo ao estabelecer um limite superior aceitável de 5 segundos para animações sem controle. O eMAG, por usa vez, adota uma postura mais rígida de exigir controle para "qualquer animação", mas que parece ser uma escolha deliberada, tendo em vista que as orientações do WCAG 2.0 já eram disponíveis na época de redação do eMAG. Por isso, esse aspecto não foi considerado uma defasagem.

Além disso, o eMAG apresenta um texto um tanto ambíguo para essa recomendação. Nele, é dito que:

> "Conteúdos como slideshows, que 'se movem', rolagens, movimentações em geral ou animações não devem ser disparadas automaticamente **sem o controle do usuário**, mesmo em propagandas na página."

Fica um pouco dúbio aqui qual das seguintes interpretações da proibição do eMAG é a correta, a depender sobretudo da maneira em que se interpreta o termo "*sem o controle do usuário*":

1) Ao interpretar que o termo "*sem o controle do usuário*" reforça/explica a ideia de animações que disparam de maneira automática sem o desejo do usuário, a orientação passa a proibir que animações automáticas de maneira geral sejam empregadas.

2) Ao interpretar que "*sem o controle do usuário*" é um termo restritivo em que são tratadas particularmente as animações que se iniciam automaticamente sem os botões que fornecem controle para o usuário, então a orientação proíbe apenas as animações automáticas as quais não fornecem esse tipo de controle.

Em termos sintáticos e semânticos ao pé da letra da Língua Portuguesa, o termo inserido sem a presença de uma vírgula anterior demonstraria uma ideia de "restrição", apontando para a segunda interpretação. Logo, foi ela a adotada na adaptação do checklist. Em outras palavras, a proibição não está em usar animações automáticas em si, e sim, em usá-la sem que seja disponibilizada uma forma de controle ao usuário.

Portanto:
- O texto foi reescrito para que fosse menos ambíguo e mais enxuto na descrição do item no checklist, mantendo a essência da recomendação.
- Um exemplo de aplicação utilizando `prefers-reduced-motion` como prática moderna de redução de movimento de elementos da página foi acrescentado, baseado no exemplo fornecido pela [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion).

----------------------------------------------------------------------------

### 3 Conteúdo/Informação

#### 3.1 Identificar o idioma principal da página

----------------------------------------------------------------------------

#### 3.2 Informar mudança de idioma no conteúdo

----------------------------------------------------------------------------

#### 3.3 Oferecer um título descritivo e informativo à página

----------------------------------------------------------------------------

#### 3.4 Informar o usuário sobre sua localização na página

----------------------------------------------------------------------------

#### 3.5 Descrever links clara e sucintamente

----------------------------------------------------------------------------

#### 3.6 Fornecer alternativa em texto para as imagens do sítio

----------------------------------------------------------------------------

#### 3.7 Utilizar mapas de imagem de forma acessível

----------------------------------------------------------------------------

#### 3.8 Disponibilizar documentos em formatos acessíveis

**Defasagem do eMAG: nível leve**

Esse talvez seja um dos itens mais difíceis de analisar a defasagem pelo fato de não haver um Critério de Sucesso do WCAG que seja indicado como fonte ou inspiração. O epicentro da dificuldade está na orientação:

> "Se um arquivo for disponibilizado em PDF, deverá ser fornecida uma alternativa em HTML ou ODF"

É possível conjecturar possíveis razões para ela:

1) Historicamente, o formato PDF apresentava sérios problemas em termos de acessibilidade, que só passaram a ser endereçados com a norma [ISO 14289-1 (PDF/UA)](https://pdfa.org/resource/iso-14289-pdfua) em 2012. O próprio WCAG, inclusive, enumera uma série de [técnicas para tornar documentos em PDF acessíveis](https://www.w3.org/WAI/WCAG22/Techniques/#pdf). No entanto, mesmo assim, ainda é extremamente comum encontrar PDFs inacessíveis, por uma série de razões. Talvez na época de redação do eMAG 3.1 (2014), a acessibilidade do PDF ainda não estava tão consolidada, e os autores julgaram ser melhor requerer que formatos alternativos acessíveis fossem disponibilizados.

2) Outro ponto da discussão passa pelo fato do PDF só ter sido elevado a um padrão aberto em 2008. O ODF, por definição, desde sempre foi um padrão aberto (assim como o HTML). Historicamente, há uma tendência de instituições governamentais preferirem padrões abertos e softwares livres como forma de garantir mais autonomia e segurança em governança eletrônica (algo estabelecido inclusive no [Padrões de Interoperabilidade de Governo Eletrônico - ePING](https://eping.governoeletronico.gov.br/), e talvez por isso a recomendação siga a linha dos formatos alternativos.

No entanto, o fato é que hoje o PDF é um padrão aberto e com suporte a acessibilidade, o que levanta um ponto em relação a defasagem do eMAG. Pode até ser discutível se a acessibilidade de documentos HTML e ODF é mais fácil de ser garantida. Alguns sites governamentais, como o [Government Digital Service do Reino Unido](https://www.gov.uk/guidance/publishing-accessible-documents), o [Section 508 dos EUA](https://www.section508.gov/create/pdfs/) e o [Web Accessibility Guide da Nova Zelândia](https://govtnz.github.io/web-a11y-guidance/wct/pdf-and-office-documents/publishing-pdf-and-office-documents.html) ainda especificam que haja preferência por HTML em detrimento do PDF.

Ainda assim, há exemplos de publicações de documentos em PDF do GOV.BR que não possuem alternativa em HTML ou ODF (por exemplo, alguns [editais do CPNU](https://www.gov.br/gestao/pt-br/concursonacional/editais)) e fica difícil dizer se essa recomendação deixou de ser adotada oficialmente ou se esses são de fato erros de acessibilidade. O grande cerne da questão portanto se torna: disponibilizar um documento somente no formato PDF, porém garantindo a sua acessibilidade, seria suficiente para cumprir essa recomendação? A sugestão de formatos alternativos é uma necessidade na visão do eMAG ou apenas uma padronização?

É impossível ter certeza na resposta desses questionamentos sem que isso seja clarificado diretamente no eMAG ou pelos seus autores. Dito isso, foi considerado que, pelo fato de hoje o PDF ser um padrão aberto e com suporte à acessibilidade, ele pode ser suficiente desde que o documento seja de fato acessível, ainda que o formato HTML seja preferível.

Portanto:
- Foi reconhecida na descrição do item no checklist a possibilidade do formato PDF ser utilizado de maneira suficiente, desde que a acessibilidade do documento seja garantida. Ainda assim, ressaltou-se que a preferência ainda deve ser sobretudo para o formato HTML.
- Uma nova referência às [Técnicas do WCAG para tornar documentos em PDF acessíveis](https://www.w3.org/WAI/WCAG22/Techniques/#pdf)

----------------------------------------------------------------------------

#### 3.9 Em tabelas, utilizar títulos e resumos de forma apropriada

----------------------------------------------------------------------------

#### 3.10 Associar células de dados às células de cabeçalho

----------------------------------------------------------------------------

#### 3.11 Garantir a leitura e compreensão das informações

----------------------------------------------------------------------------

#### 3.12 Disponibilizar uma explicação para siglas, abreviaturas e palavras incomuns

----------------------------------------------------------------------------

### 4 Apresentação/Design

#### 4.1 Oferecer contraste mínimo entre plano de fundo e primeiro plano

**Defasagem do eMAG: nível leve**

A recomendação permanece tecnicamente válida e alinhada ao critério 1.4.3 do WCAG. Contudo, o eMAG adota uma abordagem que parece ser deliberadamente simplificada ao exigir contraste mínimo de 4,5:1 para todos os casos e ao desaconselhar o uso de imagens de fundo atrás do texto.

O WCAG 2.0 da época, por exemplo, flexibiliza o contraste mínimo para 3:1 em alguns cenários especiais no [Critério de sucesso 1.4.3: Contraste Mínimo](https://www.w3.org/TR/WCAG20/#visual-audio-contrast). Além disso, também não proibi o uso de imagens como fundo, apenas orienta que o fundo (seja uma imagem ou não) atenda o contraste mínimo ([Técnica G18](https://www.w3.org/TR/2016/NOTE-WCAG20-TECHS-20161007/G18)). Ele inclusive chega a citar que o fundo pode ser sombreado para atender o contraste mínimo, sugerindo indiretamente o uso de CSS para esse objetivo.

Essas decisões provavelmente refletem uma estratégia de padronização e simplificação da auditoria de acessibilidade em portais governamentais. Embora atualmente existam técnicas consolidadas que permitem garantir contraste adequado mesmo com imagens de fundo, a orientação do eMAG não induz a erros técnicos, apenas restringe possibilidades de design. Assim, caracteriza-se uma defasagem leve, mas adotou-se uma abordagem conservadora de não alterar as recomendações originais do eMAG.

É válido ainda notar que o WCAG na versão 2.1, posterior ao eMAG 3.1, apresentou em seu texto, por sua vez, um novo [Critério de Sucesso 1.4.11 Contraste Não textual](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/#non-text-contrast) que estabelece a proporção mínima de 3:1 para contraste entre alguns elementos não textuais, quase como um outro cenário excepcional à regra do contraste 4,5:1. Não só isso, como no WCAG 2.2 foi adicionado ainda um outro [Critério de Sucesso 2.4.13 Aparência do Foco](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#focus-appearance) que também estabelece contraste mínimo de 3:1 para a borda dos elementos focáveis. No entanto, como os outros casos especiais de 3:1 não foram abordados no eMAG, provavelmente pelas razões já citadas, e também decidiu-se não atualizá-los neste checklist, extrapolou-se que também não faria sentido portar essas novas exeções dos critérios de sucesso.

Portanto:
- As orientações bases não foram alteradas, mesmo teoricamente com elas configurando uma leve defasagem.
- Os exemplos foram melhorados para demonstrar a aplicação das cores de fundo e primeiro plano com CSS.
- Foi deixado mais claro na descrição do item o mínimo recomendado para o contraste numa folha de alto contraste, já que isso só estava sendo especificado no exemplo de aplicação.
- Um exemplo de má prática de foco com contraste insuficiente foi adicionado para que os inspetores também se atentem a esse aspecto. Esse exemplo conversa diretamente com a recomendação "Possibilitar que o elemento com foco seja visualmente evidente" e seus respectivos exemplos.

----------------------------------------------------------------------------

#### 4.2 Não utilizar apenas cor ou outras características sensoriais para diferenciar elementos

**Defasagem do eMAG: nível nulo**

A recomendação permanece muito relevante no contexto de acessibilidade atual, e não apresenta pontos de defasagem notáveis. Os exemplos dados são simples, mas a diferenciação dos elementos via indicação por texto feita no exemplo não é a única maneira sugerida pelo eMAG. Trata-se de um exemplo ilustrativo.

Portanto:

- Manteve-se a essência do texto e dos exemplos originais, com pequenas mudanças na descrição da recomendação para deixá-la mais enxuta nesse checklist, e no exemplo para deixá-lo mais didático.

----------------------------------------------------------------------------

#### 4.3 Permitir redimensionamento sem perda de funcionalidade

**Defasagem do eMAG: nível moderado**

No eMAG, essa recomendação referencia o [Critério de sucesso 1.4.4: Redimensionar Texto do WCAG 2.0](https://www.w3.org/TR/WCAG20/#visual-audio-contrast-scale). Esse critério do WCAG trata particularmente do redimensionamento de **texto**, sem perda de funcionalidade e conteúdo, em até 200%. O eMAG, por sua vez, extrapola o redimensionamento não só para o texto, mas para os elementos da página em geral.

A questão é que, na época de redação do eMAG, o WCAG 2.0 parecia só abordar o redimensionamento de texto, de maneira mais específica. No entanto, com o lançamento da versão WCAG 2.1, um novo [Critério de Sucesso 1.4.10 Realinhar](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/#reflow) foi incluído como forma de complementar mais a discussão em torno do redimensionamento abordando elementos de maneira geral da página (similar ao que o eMAG discutia). O ponto é que, de acordo com esse critério, o limite superior do zoom para manutenção de informação, funcionalidade e sem rolagem horizontal (esse último com algumas exceções) é de 400%, o dobro do que o eMAG estipulava.

O fato estranho é que, por mais que os critérios 1.4.4 e o 1.4.10 tenham abordagens um pouco diferentes, o critério 1.4.10 parece uma generalização mais ampla do 1.4.4, de forma que o cumprimento 1.4.10 parece garantir (pelo menos na maioria das vezes) o cumprimento do 1.4.4. Em outras palavras, garantir a funcionalidade e a manutenção de informação da página em zoom de 400% normalmente já garante a compreensibilidade do texto dela em zoom de 200% de maneira natural.

Além disso, o critério 1.4.10 estabelece algumas exceções para elementos em que pode ocorrer o aparecimento da barra horizontal, definindo como válido para:

> "partes do conteúdo que requerem layout bidimensional para uso ou significado" 

Por exemplo:

> "imagens, mapas, diagramas, vídeos, jogos, apresentações, tabelas de dados e interfaces em que seja necessário manter barras de ferramentas à vista ao se manipular conteúdo".

O cumprimento à recomendação do eMAG hoje, na forma que está, pode garantir a aderência ao critério 1.4.4 do WCAG e até contribuir para fornecer boa acessibilidade para a página, mas pode falhar no critério 1.4.10. Por isso, a defasagem foi classificada como de nível moderado.

Portanto:
- O limite superior para manutenção da compreensibilidade e funcionalidade da página foi aumentado de 200% para 400%, vide o novo critério 1.4.10 do WCAG 2.1.
- Exceções para a validez do aparecimento da barra horizontal ao fazer o zoom foram estabelecidas, vide o novo critério 1.4.10 do WCAG 2.1.
- Além do emprego de diferentes folhas de estilo, o uso de *media queries* do CSS foi citado como possível abordagem para garantir a responsividade da página em diferentes resoluções de tela ou zooms.
- O primeiro exemplo com imagens de um site em redimensionamento de 200% foi descartado, visto que o novo limite é 400%.
- O outro exemplo com imagem de layout responsivo foi mantido
- Uma nova referência ao critério de sucesso 1.4.10 foi adicionada.

----------------------------------------------------------------------------

#### 4.4 Possibilitar que o elemento com foco seja visualmente evidente

**Defasagem do eMAG: nível leve**

A ideia central da recomendação de que elementos devem ter foco visível continua atual e relevante em termos de acessibilidade. No entanto, a recomendação apresenta alguns pontos de defasagem leves que valem a pena serem notados.

Em primeiro lugar, o exemplo do eMAG ilustra a estilização da borda dos elementos utilizando a propriedade `border`. Atualmente, entretanto, a boa prática dita que a estilização da borda ao focar em um elemento deve ser feita utilizando a propriedade `outline`. Isso porque `outline`, ao contrário de `border`, não faz parte do cálculo do espaço do elemento. Por isso, quando `border` é utilizado com uma certa espessura, o tamanho total do elemento aumenta em e isso pode empurrar os elementos ao redor, causando o efeito desagradável de *layout shift* (veja mais em [Outline - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/outline#description) e [Border - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border#borders_vs._outlines). Esse é o ponto principal que leva a classificar defasagem como leve.

Além disso, há ainda um outro pequeno ajuste no exemplo que poderia ser feito. Atualmente, em algumas situações é costumeiro desenvolvedores optarem pela pseudo-classe do CSS `:focus-visible` ao invés da classe `:focus` sugerida. Isso porque, ao utilizar `:focus` em um botão configurando a propriedade `outline`, por exemplo, o destaque para a borda não é apenas aplicado ao botão durante a navegação pelo teclado, mas também brevemente quando ele é pressionado. A pseudo-classe `:focus-visible`, por outro lado, garantiria que a borda só seria destacada pela navegação do teclado, a omitindo quando o botão fosse clicado.

Portanto:

- A propriedade `border` do exemplo foi substituída por `outline`

- A pseudo-classe `:focus` foi substituída por `:focus-visible`

- Um exemplo de má prática que retira o foco visual com `outline: none` foi adicionado, e uma explicação histórica contextualizando o porquê de alguns desenvolvedores tomarem essa decisão inacessível foi explicitada.

----------------------------------------------------------------------------

### 5 Multimídia

#### 5.1 Fornecer alternativa para vídeo

**Defasagem do eMAG: nível moderado**

Toda a ideia central da recomendação é relevante para o contexto de acessibilidade atual. Os maiores problemas se encontram no último exemplo da recomendação, em que o eMAG demonstra o uso do elemento `<video>` do HTML5. Alguns são discutidos a seguir.

Em primeiro lugar, o último exemplo apresenta controle redundante no elemento `<button onclick="playPause()">Play/Pause</button>` para reger o elemento `<video>`. A questão é que o próprio elemento `<video>` possui o atributo `controls` que já faz com que o navegador renderize seu próprio player acessível nativo ([Elemento video - MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/video)). Ao inserir botões customizados logo acima de um vídeo que já possui controles nativos, cria-se uma interface duplicada que pode ser confusa, especialmente para usuários de tecnologias assistivas. Não só isso, mas o elemento redundante de controle adicionado possui acessibilidade ainda pior que o elemento padrão, uma vez que não atualiza seu texto ou atributo (como `aria-pressed` ou `aria-label`) para informar dinamicamente se a ação é reproduzir ou pausar, deixando o usuário sem feedback de estado adequado. Uma pouco dessa problemática é discutido no [Critério de Sucesso 4.1.2: Nome, Função, Valor](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html).

Em segundo lugar, a abordagem de se utilizar os botões "Pequeno", "Médio" e "Grande" para alterar o tamanho do vídeo, pelo menos da forma que foi feita, não é a melhor prática. Isso porque o valor da largura do vídeo é modificado via JavaScript com valores absolutos em pixels, o que pode quebrar a responsividade. Uma possível forma de melhorar isso seria via CSS utilizando a propriedade `max-width: 100%` para o elemento do vídeo, garantindo que ele ocupe o tamanho total de seu contêiner, mas não o ultrapasse. O contêiner, por sua vez, poderia ser manipulado conforme a necessidade do desenvolvedor para garantir a responsividade e a correta disposição dos elementos da página. Há mais detalhes sobre essa discussão que pode ser visto na [MDN Web Docs - Images, media, and form elements](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Images_media_forms).

Ainda na linha dos problemas, o uso de eventos inline (`onclick` diretamente no elemento HTML) é hoje considerado uma má prática arquitetônica e de segurança. A [MDN Web Docs em "Inline event handlers — don't use these"](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Events#inline_event_handlers_%E2%80%94_dont_use_these) é diretamente contra essa prática, e recomenda o uso da abordagem com `addEventListener` ao invés.

Há ainda uma inconsistência com o que é dito no texto da recomendação em si: se por um lado foi recomendado que legendas e descrições sejam fornecidas, por outro o exemplo dado não segue essa orientação. Isso poderia ter sido feito com o uso do elemento `<track>`, já especificado no HTML5 ([Elemento Track - MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/track) e [The track element - HTML Living Standard](https://html.spec.whatwg.org/multipage/media.html#the-track-element).

O exemplo pode induzir a alguns problemas em razão da forma que foi formulado, mas não é tratado como o principal exemplo, uma vez que está numa subseção que fala do elemento `<video>` do HTML5, e não é especificado como um padrão a ser seguido, sendo portanto mais ilustrativo. Portanto, a defasagem não é crítica e foi classificada como moderada.

Portanto:

- Os exemplos com imagem do eMAG foram reproduzidos, com um texto mais detalhado explicando algumas nuances de cada exemplo.

- No caso do exemplo 2, de vídeo com legenda, um código HTML ilustrativo que poderia refletir o que a imagem mostra foi elaborado, utilizando os elementos `<video>`, `<source>` e `<track>` do HTML5.

- O último exemplo apresentando o elemento `<video>` do HTML5 citado no eMAG foi descartado por conter os problemas já citados. A apresentação desse elemento ficou a encargo do trecho de código adicionado ao exemplo 2.

- Textos alternativos melhorados para as imagnes de exemplo foram elaborados.

----------------------------------------------------------------------------

#### 5.2 Fornecer alternativa para áudio

**Defasagem do eMAG: nível nulo**

A recomendação continua relevante no contexto de acessibilidade e não apresenta defasagens notáveis.

Portanto:

- O exemplo fornecido pelo eMAG foi reproduzido.

- As orientações gerais do eMAG foram mantidas.

- Um texto alternativo melhorado para a imagem de exemplo foi elaborado.

----------------------------------------------------------------------------

#### 5.3 Oferecer audiodescrição para vídeo pré-gravado

**Defasagem do eMAG: nível nulo**

O conceito central da Recomendação 5.3 permanece intacto e perfeitamente alinhado com as diretrizes atuais, como WCAG 2.1 e 2.2. A exigência de que conteúdos visuais cruciais sejam descritos sonoramente atende diretamente ao [Critério de Sucesso 1.2.5: Audio Description (Prerecorded)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#audio-description-prerecorded), que é um requisito de nível AA. Inclusive, a definição técnica fornecida pelo eMAG sobre como a audiodescrição deve ser sincronizada é a [definição exata adotada pelo WCAG 2.2](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#dfn-audio-descriptions).

Portanto:

- O exemplo fornecido pelo eMAG foi reproduzido.

- As orientações gerais do eMAG foram mantidas.

- Um texto alternativo melhorado para a imagem de exemplo foi elaborado.

----------------------------------------------------------------------------

#### 5.4 Fornecer controle de áudio para som

**Defasagem do eMAG: nível moderado**

As orientações gerais dessa recomendação continuam atuais e alinhadas com diretrizes de acessibilidade. No entanto, há pontos de defasagem notáveis no exemplo de código dado, e também há uma discussão relevante acerca de áudios reproduzidos automaticamente que não foi abordada no texto original.

Em primeiro lugar, o exemplo apresenta controle redundante no elemento `<button onclick="playPause()">Play/Pause</button>` para reger o elemento `<audio>`. A questão é que o próprio elemento `<audio>` possui o atributo `controls` que já faz com que o navegador renderize seu próprio player acessível nativo ([Elemento video - MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/audio)). Ao inserir um botão customizados logo acima de um áudio que já possui controles nativos, cria-se uma interface duplicada que pode ser confusa, especialmente para usuários de tecnologias assistivas. Não só isso, mas o elemento redundante de controle adicionado possui acessibilidade ainda pior que o elemento padrão, uma vez que não atualiza seu texto ou atributo (como `aria-pressed` ou `aria-label`) para informar dinamicamente se a ação é reproduzir ou pausar, deixando o usuário sem feedback de estado adequado. Uma pouco dessa problemática é discutido no [Critério de Sucesso 4.1.2: Nome, Função, Valor](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html). Aliás, é importante notar que o eMAG no texto logo antes desse afirma que o elemento `<audio>` "deve receber controles de play, pause e stop", o que pode acabar induzindo o leitor a pensar equivocadamente que os controles personalizados via HTML e JS devem ser implementados junto ou no lugar dos controles padrões definidos pelo atributo `controls`. 

Em segundo lugar, o uso de eventos inline (`onclick` diretamente no elemento HTML) no exemplo é hoje considerado uma má prática arquitetônica e de segurança. A [MDN Web Docs em "Inline event handlers — don't use these"](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Events#inline_event_handlers_%E2%80%94_dont_use_these) é diretamente contra essa prática, e recomenda o uso da abordagem com `addEventListener` ao invés.

Saindo dos problemas do exemplo fornecido, há uma discussão relevante que não foi abordada no texto original: a de áudios que tocam automaticamente ao abrir a página. No eMAG, esse ponto sequer é mencionado (e tampouco proibido ou criticado). No WCAG (2.0, 2.1, 2.2), ele não é proibido expressamente, mas há um comentário na página [Entendendo o Critério de Sucesso 1.4.2: Controle de Áudio](https://www.w3.org/WAI/WCAG22/Understanding/audio-control.html) que afirma que essa prática é "desencorajada", especialmente se o som dura mais de 3 segundos. Essa discussão merece um destaque especial tendo em vista que o áudio que toca automaticamente numa página pode dificultar a orientação do usuário, especialmente dos que usam tecnologias assistivas, uma vez que ele pode conflitar e abafar a voz dos leitores de tela, além de poder ser inconveniente. O WCAG vai um pouco mais além e ainda fornece técnicas em que [um som reproduzido automaticamente é parado dentro de 3 segundos (G171)](https://www.w3.org/WAI/WCAG22/Techniques/general/G171) e em que [um controle próximo ao início da página para parar o som automático é providenciado (G170)](https://www.w3.org/WAI/WCAG22/Techniques/general/G170).

Pelas razões acima, a defasagem foi classificada como moderada.

Portanto:

- Uma discussão breve acerca de áudios que são reproduzidos automaticamente foi adicionada à descrição do item e aos critérios de verificação. Assim como o eMAG e o WCAG, essa prática não foi expressamente proibida, mas desencorajada. Reforçou-se que, caso adotada, controles para tal áudio fáceis de serem encontrados, como no início da página, devem ser providenciados.

- Um reforço de que "Silenciar o áudio no sistema não é suficiente para atender essa recomendação", conforme diz também o WCAG no critério 1.4.2.

- O exemplo de código do eMAG foi reformulado para utilizar somente os controles padrões fornecidos pelo atributo `controls`. Uma descrição mais completa para o exemplo também foi feita.

- Um novo exemplo de código com um áudio que toca automaticamente e apresenta controle para parar o som logo no início da página foi adicionado. Esse controle não é nativo do atributo `controls`, e é manipulado via JavaScript para informar dinamicamente se a ação é reproduzir ou pausar, fornecendo feedback adequado ao usuário. Além disso, o uso de `onclick` diretamente no elemento HTML foi evitado, optando pelo uso de `addEventListener`. Por fim, esse exemplo não foi marcado como boa prática, e sim como prática neutra, para não induzir o leitor a pensar que o autoplay do áudio seja uma prática recomendada. Essa constatação também está presente na descrição do exemplo.

----------------------------------------------------------------------------

#### 5.5 Fornecer controle de animação

**Defasagem do eMAG: nível nulo**

A recomendação em si não apresenta nenhum ponto grave de defasagem. No WCAG 2.0, o [Critério de Sucesso 2.2.2: Colocar em pausa, parar e ocultar](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-pause.html), ao qual essa recomendação referencia, é um pouco mais flexível, sobretudo ao estabelecer um limite superior aceitável de 5 segundos para animações. O eMAG, por usa vez, adota uma postura mais rígida de exigir controle para "qualquer animação", mas que parece ser uma escolha deliberada, tendo em vista que as orientações do WCAG 2.0 já eram disponíveis na época de redação do eMAG. Por isso, esse aspecto não foi considerado uma defasagem.

Quanto ao exemplo com o gif, não fica claro como foi feita a implementação do mecanismo de pausa da animação, uma vez que o elemento `<img>` renderizando um arquivo .gif não possui um mecanismo nativo para ser pausado ou iniciado. Mesmo assim, o exemplo cumpre o propósito de ilustrar a orientação da recomendação, ainda que não se preocupe com detalhes de implementação.

O real problema dessa recomendação é que ela parece ser redundante em relação à recomendação 2.7 "Assegurar o controle do usuário sobre as alterações temporais do conteúdo", na qual é dito que:

> "Conteúdos como slideshows, que 'se movem', rolagens, movimentações em geral ou animações não devem ser disparadas automaticamente sem o controle do usuário, mesmo em propagandas na página. [...] Além disso, o usuário deve ser capaz de parar e reiniciar conteúdos que se movem, sem exceção.".

Enquanto a recomendação 5.5 afirma que:

> "Para qualquer animação que inicie automaticamente na página devem ser fornecidos mecanismos para que o usuário possa pausar, parar ou ocultar tal animação"


Tratando justamente da mesma orientação com palavras diferentes. As duas, inclusive, referenciam ao mesmo Critério de Sucesso 2.2.2.

Como a recomendação 5.5 está dentro da categoria "Multimídia", foi considerado que ela é apenas um reforço positivo da recomendação 2.7 para os casos de animações atreladas a elementos midiáticos (como os gifs citados pela recomendação).

Portanto:
- Toda a ideia da recomendação foi mantida e foi dada uma ênfase maior ao fato dela tratar das "animações de mídia" de maneira mais específica.

----------------------------------------------------------------------------

### 6 Formulários

#### 6.1 Fornecer alternativa em texto para os botões de imagem de formulários

**Defasagem do eMAG: nível moderado**

Sob um certo ponto de vista, essa recomendação pode ser vista como uma redundância em relação à recomendação 3.6 "Fornecer alternativa em texto para as imagens do sítio". Seu núcleo, portanto, permanece válido, afinal é o mesmo que o da recomendação citada. Sua especificidade se justifica no eMAG em função da orientação de algumas práticas adicionais ligadas ao contexto de botões de formulário. No entanto, alguma dessas práticas hoje podem ser consideradas defasadas.

O texto original do eMAG sugere formas de se fornecer texto alternativo para botões do tipo imagem. Ele corretamente orienta o uso do atributo `alt` em botões `<input type="image">`, por mais que esse tipo possa não ser tão comum atualmente. O ponto central de defasagem está quando o texto afirma:

> "Já para outros tipos de botões (reset e button), é preciso substituir o botão pela imagem que se deseja utilizar através do CSS. Nesse caso, para que o botão seja acessível, ele deve possuir um value descritivo, conforme o exemplo a seguir."

E em seguida fornece um exemplo de aplicação em que o texto do botão é escondido utilizando `text-indent:-20000px;` no CSS. Em primeiro lugar, a prática de se utilizar CSS para aplicar imagens de fundo a botões, embora possível, não é muito recomendada no contexto atual. Hoje em dia, é bem mais aconselhado empregar o elemento `<button>` com um elemento filho `<img>` para aplicar a imagem no botão, estilizando os elementos de acordo via CSS ([O elemento button - MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Elements/button)). Portanto, afirmar que é "*preciso substituir o botão pela imagem que se deseja utilizar através do CSS*" não é necessariamente verdade no contexto atual de desenvolvimento.

Além disso, o segundo exemplo de aplicação do texto induz à prática de esconder o conteúdo textual do botão utilizando o CSS via `text-indent` (conhecido como *Phark Method*), algo que pode ser problemático por diversas razões (uma delas é tratada em [Invisible Content - WebAIM](https://webaim.org/techniques/css/invisiblecontent/)). Há métodos mais aconselhados para alcançar esse objetivo, como discutido em [Note on Hiding Elements - Web Accessibility Initiative (WAI) - W3C](https://www.w3.org/WAI/tutorials/forms/labels/#note-on-hiding-elements).

Como o uso de CSS para aplicar imagens de fundo a botões é tratado como única ou principal maneira para alcançar o objetivo, e como o exemplo ilustrando como fazer isso utiliza uma técnica que pode induzir problemas, a defasagem da recomendação foi classificada como moderada.

Portanto:
- A descrição do item foi reformulada para ficar mais enxuta e estabelecer mais claramente seu propósito: deve-se fornecer alternativas textuais que explicitem claramente a função do botão para imagens que atuam como botão. Os cenários descritos pelo eMAG são tratados como exemplos.

- O cenário de utilização do CSS para aplicação da imagem ao fundo do botão foi descartado. Em seu lugar, foi citado o cenário utilizando uma imagem com texto alternativo dentro do elemento `<button>`. Os critérios de verificação e os exemplos de código correspondentes também foram substituídos.

- Um exemplo demonstrando uma maneira mais apropriada de esconder o texto do botão (e elementos em geral) foi adicionado, baseado diretamente no código disponível em [Note on Hiding Elements - Web Accessibility Initiative (WAI) - W3C](https://www.w3.org/WAI/tutorials/forms/labels/#note-on-hiding-elements).

- Um exemplo de má prática em que tanto o texto do botão quanto o atributo `alt` para a imagem do botão com os mesmos valores foi adicionado, citando que isso pode gerar uma redundância que faz leitores de tela repetirem a informação, podendo desorientar usuários.

- Uma nova referência à [Técnica H36 do WCAG: Using `alt` attributes on images used as submit buttons](https://www.w3.org/WAI/WCAG22/Techniques/html/H36) foi adicionada.

----------------------------------------------------------------------------

#### 6.2 Associar etiquetas aos seus campos

**Defasagem do eMAG: nível leve**

O núcleo central da recomendação de associar explicitamente `<label>` aos campos correspondentes usando os atributos `for` (no label) e `id` (no input) com o mesmo valor permanece plenamente válido. Há alguns pontos de atenção no exemplo de aplicação, entretanto, que merecem ser ressaltados.

Em primeira análise, no exemplo, há um elemento `<label>Sexo:</label>` solto, sem o atributo `for` e sem encapsular nenhum controle. Por mais que visualmente seja evidente a relação com os `<input>` que se seguem logo abaixo, a falta de uma associação explícita pode fazer com que leitores de tela não relacionem adequadamente esse label com as opções em seguida. No caso mostrado, isso até pode ser facilmente inferido na escuta e leitura do usuário, mas podem haver outros casos em que essa ausência acarrete num formulário mais complexo de se entender. Além disso, argumenta-se que o próprio emprego do `<label>Sexo:</label>` não seja a maneira mais adequada de se introduzir os controles em seguida. O próprio eMAG na recomendação 6.7 "Agrupar campos de formulário" afirma que:

> "É recomendado que os campos com informações relacionadas sejam agrupadas utilizando o elemento FIELDSET, principalmente em formulários longos. O agrupamento deverá ser feito de maneira lógica, associando o elemento LEGEND explicando claramente o propósito ou natureza dos agrupamentos."

Em outras palavras, o elemento `<legend>` seria mais apropriado para cumprir essa função de rótulo de uma seção de formulário que estaria agrupada dentro de um elemento `<fieldset>`. 

Além disso, o elemento `<textarea name="msg" id="msg">Digite sua mensagem</textarea>` possui um valor inicial pré-preenchido que estaria atuando como um placeholder. Essa abordagem viola em algum grau a recomendação 6.5 "Fornecer instruções para entrada de dados" do próprio eMAG, que  delimita os cenários em que caracteres pré-definidos podem ser utilizados:

> "A utilização de caracteres pré-definidos em áreas de entrada de texto só deve ocorrer se: O texto for incluído após a entrada de dados pelo usuário (por exemplo, sugerir um novo nome de usuário caso o escolhido já exista); A semântica do documento justifique a inclusão de texto pré-definido (por exemplo, uma loja virtual que só vende para determinado país já vem com o campo país preenchido); Os caracteres tenham sido fornecidos previamente pelo usuário (por exemplo, refinamento de busca)."

Como o texto da recomendação em si não possui nenhuma defasagem notável, o exemplo é tratado pela própria recomendação como ilustrativo e os problemas do exemplo não induzem a um erro grave, a defasagem da recomendação foi classificada como leve.

Portanto:

- Uma explicação melhor detalhada sobre os elementos que não necessitam do `<label>` foi adicionada na descrição do item, baseado no texto da [Técnica WCAG H44: Using label elements to associate text labels with form controls](https://www.w3.org/WAI/WCAG22/Techniques/html/H44).

- O exemplo foi refatorado para reparar os erros citados do uso incorreto do `<label>` e valor pré-definido em `<textarea>` utilizado como placeholder.

- Um exemplo de má prática foi adicionado contendo alguns erros clássicos que podem ser encontrados, como ausência de associação etiqueta-campo, associação quebrada e colisão de identificadores.

----------------------------------------------------------------------------

#### 6.3 Estabelecer uma ordem lógica de navegação

**Defasagem do eMAG: nível nulo.**

Mais uma vez, essa recomendação é de certo modo uma redundância em relação à recomendação 1.4 "Ordenar de forma lógica e intuitiva a leitura e tabulação", apenas mais voltada para o contexto de formulários. Assim como a outra, essa recomendação permanece consistente com orientações de acessibilidade atuais, mas as seguintes adaptações foram feitas no intuito de clarificar e contextualizar mais a interpretação de certos aspectos do texto original.

- Tanto na descrição do item quanto no terceiro critério de verificação foi incorporado um detalhamento maior sobre o uso do atributo `tabindex` para evitar valores maiores que 0 atribuídos e tomar cuidado caso esses valores sejam utilizados. Em outras palavras, seu uso não foi proibido (afinal, o eMAG e o WCAG não o proíbem), apenas foi melhor explicado o que seria "usar o `tabindex` com cuidado", conforme explicado pela [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Global_attributes/tabindex). Essa referência sobre o uso de `tabindex`, que ainda justifica a orientação de evitar os valores maiores que 0, também foi adicionada.

- A descrição do texto também foi incrementada para conter uma explicação mais robusta sobre o que significa uma ordem de navegação possuir uma sequência lógica, da mesma forma que foi feito no item "Ordenar de forma lógica e intuitiva a leitura e tabulação" do checklist.

- Foi acrescentada à descrição do item e à seção de referências uma referência para a recomendação 1.4 "Ordenar de forma lógica e intuitiva a leitura e tabulação", uma vez que ela está intimamente relacionada com esse item.

- Uma referência para o [Critério de sucesso WCAG 1.3.2: Sequência com Significado](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#meaningful-sequence) foi adicionada, pois esse critério está relacionado com esse item e inclusive é citado na recomendação 1.4 "Ordenar de forma lógica e intuitiva a leitura e tabulação".

----------------------------------------------------------------------------

#### 6.4 Não provocar automaticamente alteração no contexto

Defasagem do eMAG: nível leve.

A recomendação não está tecnicamente incorreta nem em desacordo com o WCAG 2.0 (vigente à época) ou as versões atuais. No entanto, há pontos relevantes que introduzem grau de defasagem a serem abordados, sobretudo em relação a uma confusão conceitual do texto do eMAG e à adoção de uma abordagem mais restritiva do que o necessário.

Em primeiro lugar, o eMAG mistura 2 conceitos distintos na sua redação: o de "receber foco" e "modificar entrada". O texto original do eMAG afirma:

> "Quando um elemento de formulário **receber o foco**, não deve ser iniciada uma mudança automática na página que confunda ou desoriente o usuário."

Ele trata, portanto, mais especificamente do recebimento de foco. No entanto, tanto os exemplos de aplicação fornecidos quanto à referência ao [Critério de Sucesso WCAG 3.2.2: Em Entrada](https://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-unpredictable-change.html) envolvem o ato de modificar a entrada -- isto é -- interagir com os campos de entrada de um formulário, por exemplo. Não só isso, como o [Critério de Sucesso WCAG 3.2.1: Em Foco](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#on-focus) sequer foi referenciado, quando possivelmente deveria ter sido.

Além disso, há uma discussão muito relevante em relação à seguinte restrição do eMAG:

> "Assim, as mudanças devem ocorrer através do acionamento de um botão."

A referência do WCAG, inclusive à versão 2.0 vigente na época de redação do eMAG, não é tão restritiva nesse sentido. Ela permite, por exemplo, a ocorrência mudanças de contexto ao modificar entradas desde que o usuário seja avisado sobre esse comportamento antes de utilizar o componente ([Critério de Sucesso WCAG 3.2.2: Em Entrada](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#on-input)). De fato, a [técnica G80 do WCAG "*Providing a submit button to initiate a change of context*"](https://www.w3.org/WAI/WCAG22/Techniques/general/G80) exemplifica uma orientação mais aderente ao que pede o eMAG, mas há outras técnicas que exemplificam a ideia de se avisar previamente sobre a mudança de contexto, como a [G13 "*Describing what will happen before a change to a form control that causes a change of context to occur is made*"](https://www.w3.org/WAI/WCAG22/Techniques/general/G13).

Argumenta-se que, como essa orientação já era mais branda no WCAG 2.0, então os autores do eMAG adotaram uma postura mais restritiva de forma deliberada. A razão dessa restrição ser antiquada é que o design de interação evoluiu muito desde então, incluindo a popularização das SPAs (*Single Page Applications*). Tratar essa rigidez como a única verdade inibe o uso de padrões modernos e seguros (como atualizações assíncronas anunciadas via `aria-live`, por exemplo), que são amplamente aceitos pelo WCAG e podem oferecer, inclusive, uma experiência de usuário melhor e mais fluida hoje em dia.

Assim, em razão desses fatores, a defasagem da recomendação foi classificada como leve.

Portanto:

- A descrição do item foi adaptada para abordar a aceitabilidade de mudanças de contexto serem desencadeadas por modificações de entrada desde que isso seja claramente e anteriormente avisado ao usuário. Ainda assim, destacou-se que é fortemente recomendável optar por comportamentos que somente desencadeiem as mudanças com o acionamento de botões, dando mais controle ao usuário de quando aplicá-las.

- A proibição da mudança de contexto desencadeada por recebimento de foco de um elemento de formulário foi mantida.

- Os exemplos bom e ruim do eMAG foram mantidos, mas com um aprofundamento maior na discussão. Isso foi feito especialmente para o exemplo negativo, em que foi realizada uma discussão mais ampla sobre o comportamento inconsistente do atributo `onchange` do `<select>`, tratando de como avisar antecipadamente da mudança automática de contexto, nesse caso, ainda não é suficiente para garantir uma boa acessibilidade.

- O [Critério de Sucesso WCAG 3.2.1: Em Foco](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#on-focus) foi adicionado como referência.

- A [Técnica WCAG G13 "*Describing what will happen before a change to a form control that causes a change of context to occur is made*"](https://www.w3.org/WAI/WCAG22/Techniques/general/G13) foi adicionada como referência.

- A [Técnica WCAG G80 "*Providing a submit button to initiate a change of context*"](https://www.w3.org/WAI/WCAG22/Techniques/general/G80) foi adicionada como referência.

----------------------------------------------------------------------------

#### 6.5 Fornecer instruções para entrada de dados

**Defasagem do eMAG: nível moderado.**

Embora o princípio da recomendação esteja alinhado com o WCAG e seja válido em termos de acessibilidade, algumas técnicas sugeridas estão desatualizadas e podem levar a implementações subótimas ou com impacto negativo na acessibilidade moderna.

Em primeira análise, o texto do eMAG traz algumas soluções superadas para indicação de campos obrigatórios ao sugerir o uso de uma imagem com atributo `alt` ou um `<span>Obrigatório</span>` ocultado (exemplos 2 e 3). Atualmente, o atributo `required` (citado pelo próprio eMAG) e outros recursos como `aria-required="true` são mais apropriados para cumprirem esse papel. É necessário ressaltar, entretanto, que indicações visuais extras para denotar um campo obrigatório ainda são requeridas, conforme destacado pela [MDN Web Docs ao tratar do atributo required](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/required#accessibility_concerns). Ainda assim, há alternativas mais modernas para as implementações sugeridas pelo eMAG. Inclusive, particularmente, o próprio exemplo 3, com uso do `<span>Obrigatório</span>` escondido, não é muito apropriado, pois a indicação de obrigatoriedade, apesar de disponível para leitores de tela, não é visível para os demais usuários, quebrando o seu propósito. Válido ainda mencionar que o método utilizado com `text-indent: -20000px;` para esconder esse elemento também é defasado, conforme discutido na análise da recomendação 6.1 "Fornecer alternativa em texto para os botões de imagem de formulários".

Em segundo plano, a apresentação do atributo `placeholder` no texto do eMAG fornece a seguinte descrição para ele:

> "Além do atributo required, o HTML5 apresenta, também, o placeholder. Ele é utilizado com os elementos INPUT e TEXTAREA para definir uma dica de preenchimento do campo. Quando o campo recebe o foco, a dica desaparece, mas é lida pelo leitor de tela."

Essa descrição gera uma ambiguidade que pode induzir o leitor a pensar que `placeholder` pode ser utilizado para fornecer instruções de preenchimento no lugar do elemento `<label>`. Essa noção é reforçada logo pelo exemplo seguinte, que apresenta um código HTML com campo de entrada para e-mail sem um label denotando esse propósito, que está indicado somente no atributo `placeholder`. O atributo `placeholder` não deve ser utilizado como uma alternativa para `<label>`, conforme afirmado explicitamente na própria [documentação do atributo no HTML Living Standard](https://html.spec.whatwg.org/multipage/input.html#the-placeholder-attribute). Além disso, a afirmação de que o `placeholder` é lido pelo leitor de tela pode não ser verdadeira para todas as tecnologias. Esse é o maior ponto de defasagem dessa recomendação, que eleva o nível para moderado.

O texto ainda é um tanto prolixo ao enumerar uma série de atributos do HTML5 tidos como "*importantes para acrescentar informações aos campos do formulário*". Dentre eles, o atributo `autofocus` é destacado:

> "autofocus: Utilizado para o foco do teclado ir diretamente ao campo que possua esse atributo quando a página com o formulário for carregada;"

O ponto é que esse encorajamento ao uso do `autofocus` é potencialmente perigoso. Referências como o MDN Web Docs advertem contra o uso do `autofocus` na maioria dos cenários, e que qualquer implementação dele deve ser cuidadosamente considerada antes, uma vez que o atributo rouba o foco inicial da página, quebrando o contexto e jogando os usuários no meio da página sem aviso, o que pode causar grande confusão.

Portanto:

- Na descrição do item no checklist, foi proporcionado ao atributo `placeholder` uma explicação mais completa sobre seu uso, advertendo que ele não deve ser utilizado para substituir o elemento `<label>`, sendo utilizado apenas como informação adicional.

- A enumeração dos diversos outros atributos do HTML5 que supostamente seriam importantes para acrescentar informações aos campos do formulário, incluindo o `autofocus`, foi suprimida.

-  As orientações acerca dos campos obrigatórios foram melhoradas, citando que eles devem ser claramente assinalados e de maneira acessível. Foi ainda alertado que o uso do caractere asterisco sozinho para indicação, sem mecanismo adicional que torne essa informação acessível a leitores de tela, não deve ser feito.

- O exemplo 1 do formato da data sendo especificado no `<label>` foi reaproveitado como um exemplo positivo.
- Os exemplos 2 e 3 de indicação de campos obrigatórios com uso de uma imagem com atributo `alt` ou um `<span>Obrigatório</span>` ocultado foram descartados. Em seu lugar, 2 exemplos, um bom e outro ruim, de indicação de campos obrigatórios foram apresentados, explicando com mais detalhes algumas peculiaridades e pontos de atenção ao implementar esse mecanismo.

- O exemplo de uso do `placeholder` foi reaproveitado, porém como um exemplo negativo, uma vez que o `placeholder` nele atua como única fonte de instrução de entrada de dados. Uma contraparte de exemplo positivo foi adicionado.

----------------------------------------------------------------------------

#### 6.6 Identificar e descrever erros de entrada de dados e confirmar o envio das informações

**Defasagem do eMAG: nível moderado.**

A validação de formulários em HTML é uma temática que pode ser complexa por não englobar apenas uma forma de realizá-la, abrangendo diversos métodos de diferentes ferramentas e frameworks. Nesse sentido, a recomendação em si continua bastante válida e pertinente no contexto, sobretudo por não restringir apenas uma forma de cumpri-la. A orientação em si é bem clara:

> "Quando um erro de entrada de dados for automaticamente detectado, o item que apresenta erro deve ser identificado e descrito ao usuário por texto."

O que se segue depois são exemplos de como cumprir essa recomendação adequadamente. E é nessa seção de exemplos que alguns pontos merecem ser analisados com mais atenção.

O primeiro exemplo da seção não é problemático. De fato, ele não contém nenhuma implementação de código explícita: ilustra apenas o formulário de um site que atende os requisitos de acessibilidade no que tange à identificação e descrição dos erros no formulário. Os detalhes de implementação são abstraídos, de forma que diversos métodos poderiam ser aplicados para alcançar esse resultado.

O grande centro de discussão dos exemplos está quando o texto aborda a validação de formulários nativa no lado do cliente utilizando o recurso do atributo `type` do elemento `<input>`. Esse método de validação não está de todo o errado, mas a forma que o eMAG o apresenta pode levar o leitor a pensar que a forma em que o recurso é apresentado na redação é suficiente para a garantia de boa acessibilidade, o que não é verdade. O [Critério de Sucesso 3.3.1 : Identificação do Erro, do WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/error-identification#user-agent-native-html-form-validation) enumera uma série de problemáticas da validação de formulário nativa do HTML e navegadores, demonstrando que ela pode não ser suficiente a depender do agente de usuário utilizado. O texto falha em citar mecanismos que são de fato são centrais na certificação de acessibilidade, como o uso correto dos atributos `aria-invalid`, `aria-errormessage`, `aria-describedby`, `aria-live`, entre outros. É bastante compreensível que a gama complexa de maneiras que esses mecanismos podem ser utilizados dificulta tratar de todos eles no texto, mas como o eMAG entra no mérito de detalhes de implementação utilizando somente a validação nativa do HTML5, eles ao menos deveriam ser mencionados.

Além disso, a validação de formulário nativa utilizando o atributo `type` é um tanto limitante e engessada. Há um número limitado de tipos para validação (citados no eMAG) e as indicações visuais que aparecem quando ocorre algum erro não costumam ser personalizáveis. Por isso, muitas vezes é necessário recorrer a codificação em JavaScript para fazer essa validação. Mais uma vez, como o texto entra no mérito de implementações de validação, pelo menos um exemplo de validação via linguagem de programação poderia ter sido feita. O próprio WCAG fornece alguns exemplos do tipo em algumas de suas técnicas, utilizando tanto JQuery quanto JavaScript puro, tais como [ARIA21: Using aria-invalid to Indicate An Error Field](https://www.w3.org/WAI/WCAG22/Techniques/aria/ARIA21), [SCR18: Providing client-side validation and alert](https://www.w3.org/WAI/WCAG22/Techniques/client-side-script/SCR18) e o [ARIA19: Using ARIA role=alert or Live Regions to Identify Errors](https://www.w3.org/WAI/WCAG22/Techniques/aria/ARIA19). A MDN Web Docs também estabelece alguns exemplos em [ARIA: aria-invalid attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-invalid) e [ARIA: aria-errormessage attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-errormessage).

Por fim, existe um erro de digitação no documento oficial do eMAG que gera um erro técnico. O HTML5 nunca possuiu para o atributo `type` de `<input>` os valores `"datatime"` ou `"datatime-local"`. Mesmo corrigindo a grafia para `"datetime"`, esse tipo foi removido da especificação do HTML Living Standard anos atrás. Hoje, os desenvolvedores devem utilizar exclusivamente `"datetime-local"` ou separar as entradas em `"date"` e `"time"`.

Em razão desses fatores, a defasagem foi classificada como moderado.

Portanto:

- Foi melhor esclarecido na descrição desse item que o mecanismo padrão de validação implementado puramente em HTML não é suficiente para boa garantia de acessibilidade. Estratégias extras ligadas ao ARIA foram sugeridas como possíveis abordagens para cumprir esse papel, mas não foram forçadas como regras.

- A enumeração dos possíveis valores para o atributo `type` de `<input>` foi descartada.

- O primeiro exemplo do eMAG mais alto nível mostrando como um determinado sistema se comportava com erros de validação de um formulário de cadastro foi mantido.

- O exemplo de código do eMAG utilizando apenas o mecanismo de validação padrão, com elemento `<input type="email" required>`, foi tratado como uma má prática. Foi explicado no exemplo que o problema não está no uso do mecanismo em si, mas sim, na falta de alguma estratégia adicional para melhoria de acessibilidade.

- Um exemplo extra de código foi criado demonstrando o uso de JavaScript puro e ARIA para criação de um mecanismo de validação de formulário mais robusto e acessível. Esse código foi criado baseado nos exemplos das referências citadas do WCAG e MDN Web Docs.

----------------------------------------------------------------------------

#### 6.7 Agrupar campos de formulário

**Defasagem do eMAG: nível nulo.**

Não há nada de defasado na recomendação. A ideia central de agrupar campos de formulário utilizando `<fieldset>`, `<legend>` e `<optgroup>` continua válido e previsto no HTML Living Standard[https://html.spec.whatwg.org/multipage/form-elements.html#the-fieldset-element]. Ela permanece sendo a prática mais adequada, correta e recomendada pelos padrões atuais de acessibilidade e semântica web. A própria referência feita pelo eMAG às técnicas [H71: "Providing a description for groups of form controls using `fieldset` and `legend` elements"](https://www.w3.org/WAI/WCAG22/Techniques/html/H71)
e [H85: "Using `optgroup` to group `option` elements inside a `select`"](https://www.w3.org/WAI/WCAG22/Techniques/html/H85) continuam reconhecidas nas versões mais recentes do WCAG. Sendo assim, a classificação da defasagem é de nível nulo.

Portanto:
- A descrição do item do checklist reflete diretamente, ainda que em outras palavras, o texto original do eMAG.
- Os exemplos fornecidos pelo eMAG foram readaptados, acrescidos apenas de uma descrição um pouco mais elaborada para eles.

----------------------------------------------------------------------------

#### 6.8 Fornecer estratégias de segurança específicas ao invés de CAPTCHA

**Defasagem do eMAG: nível crítico.**

Essa é uma recomendação bem desafiadora de ser avaliada e, sobretudo, adaptada para o cenário atual. É fato que o cerne da recomendação permanece válido: CAPTCHAs consistentes em desafios explícitos baseados em percepção humana são inerentemente inacessíveis. No entanto, a temática dos CAPTCHAs invoca uma discussão bastante complexa, que vai muito além das questões de acessibilidade.

Para começar, o eMAG acerta em problematizar os CAPTCHAs, pelo menos aqueles mais comuns na época de redação do documento, que eram sobretudo desafios explícitos baseados em percepção humana. Além de inacessíveis, eles são cada vez mais facilmente resolvidos por máquinas. O texto ainda apresenta uma orientação bastante válida: preferencialmente, outras estratégias — como limites de conexão, monitoramento, consistência nas políticas de segurança e uso de técnicas de desenvolvimento de serviços e formulários seguros — devem ser adotadas em detrimento dos CAPTCHAs clássicos.

No entanto, a problemática não é tão simples assim de resolver. Um artigo muito bom sobre a [Inacessibilidade dos CAPTCHAs (W3C)](https://www.w3.org/TR/turingtest/) discute uma série de possíveis abordagens de segurança, com suas vantagens e desvantagens tanto em termos de acessibilidade quanto em outros termos. De maneira geral, a seguinte percepção inicial pode ser extraída dele: há dois cenários de "cobertor curto" entre abordagens que podem ser identificadas dentro de um determinado espectro:

1) O primeiro cenário, num extremo, há uma abordagem de CAPTCHAs mais fáceis para humanos resolverem, porém também mais fáceis para máquinas resolverem, e no outro extremo, uma outra mais difícil para humanos, porém também mais difícil para máquinas.

2) O segundo cenário, num extremo, há uma abordagem mais acessível, mas que requer maior coleta de dados pessoais, e no outro extremo, uma abordagem menos acessível, mas que requer menor ou nenhuma coleta de dados.

O próprio artigo conclui que, no cenário atual, não há ainda uma alternativa única e ideal claramente melhor do que as outras.

> "In other words, while some CAPTCHA approaches are better than others, and while more recent approaches offer clear advantage over older approaches, there is still no single, ideal solution. It is important to exercise care that any implemented CAPTCHA technology correctly allow people with disabilities to identify themselves as human."

Isso atesta para a complexidade da discussão e de se abordar isso brevemente no checklist.

Além disso, o texto em si apresenta alguns pontos importantes de defasagem e outros deixados de fora. Em razão da idade do texto, ele ainda não evidencia algumas abordagens de segurança que são consideradas CAPTCHAs, mas que não necessitam de interação direta do usuário com o mecanismo: os chamados CAPTCHAs invisíveis, exemplificados por ferramentas modernas como o reCAPTCHA v3 ou o Cloudflare Turnstile. Por isso, problematizar os CAPTCHAs de maneira geral em termos de acessibilidade pode ser considerado equivocado, mas entende-se que os autores seguiram a percepção mais comum à época de que os CAPTCHAs se delimitam aos desafios de percepção humana. Há ainda alguns outros mecanismos de segurança, como os *honey pots* e *proof-of-work*, que podem servir para contribuir na segurança do sistema sem necessidade de interação do usuário que não foram citados.

Com toda essa complexa discussão, o ponto de defasagem da recomendação do eMAG se encontra numa orientação muito simples:

> "Caso o uso de CAPTCHA seja estritamente necessário, o mesmo deverá ser fornecido em forma de pergunta simples de interpretação (CAPTCHA Humano) [...] Tais perguntas poderão ser respondidas apenas por um ser humano. [...] Para tal, podem ser utilizadas perguntas de senso comum, como por exemplo, “qual é a cor do céu?” ou “o fogo é quente ou frio?”. Também podem ser utilizados testes matemáticos."

A sugestão de uso desses "CAPTCHAs humanos" como alternativa que **deve** ser usada quando um mecanismo do gênero for requisitado é, hoje, totalmente defasada. Além de serem facilmente quebrados, ainda mais no contexto das LLMs, o fornecimento desses CAPTCHAs e a interpretação de que eles são "suficientes" desrespeita diretamente as diretrizes de acessibilidade estabelecidas pelo WCAG, tais como o [Critério de Sucesso 3.3.8 Autenticação Acessível (Mínimo)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-minimum), o [Critério de Sucesso 3.3.9 Autenticação Acessível (Melhorado)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-enhanced) e o próprio [Critério de Sucesso 1.1.1 Conteúdo Não Textual](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#non-text-content) referenciado pela recomendação. Esse último critério estabelece que a forma de garantir a acessibilidade do CAPTCHA — ou melhor, minimizar a sua inacessibilidade — é providenciando diferentes mecanismos de CAPTCHA que utilizam modos de saída para diferentes tipos de percepção sensorial (e que sejam incluídas instruções de como acessar os mecanismos alternativos). Por essa razão, sobretudo, a defasagem da recomendação foi classificada como crítica, uma vez que há orientação que pode induzir a um erro de acessibilidade ou falsa sensação de conformidade com as diretrizes de acessibilidade mais modernas.

A complexidade da discussão impede que uma descrição detalhada no item do checklist seja feita. Com isso em vista, portanto, as seguintes medidas foram adotadas:
- Ao citar mecanismos alternativos de segurança que não requerem interações com o usuário e podem, em conjunto ou não, eventualmente substituir um CAPTCHA, foram incluídos também os filtros de spam, *honeypots*, *proof-of-work*, heurísitcas e os CAPTCHAs invisíveis (reCAPTCHA v3 ou o Cloudflare Turnstile).

- A orientação de que substituir os CAPTCHAs clássicos pelos chamados "CAPTCHAs humanos" foi descartada em função da sua defasagem. No seu lugar, foi orientado que a maneira mais adequada para os casos em que é absolutamente necessário utilizar CAPTCHA é providenciar diferentes mecanismos de CAPTCHA que empregam modos de saída para diferentes tipos de percepção sensorial, e que sejam incluídas instruções de como acessar os mecanismos alternativos.

- O caso especial dos processos de autenticação foi tratado na descrição do item, uma vez que o uso de CAPTCHAs sensoriais distintos nesse caso não é suficiente, conforme especificado no [Critério de Sucesso 3.3.8 Autenticação Acessível (Mínimo)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-minimum) e no [Critério de Sucesso 3.3.9 Autenticação Acessível (Melhorado)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-enhanced), do WCAG 2.2.

- O exemplo do eMAG do CAPTCHA clássico com letras distorcidas foi mantido como uma má prática.

- O exemplo do eMAG do CAPTCHA "humano" pedindo para escrever por extenso "quanto é dois mais três" e tratado como alternativa suficiente aos outros CAPTCHAs foi mantido, porém tratado como uma má prática, diferente do que o eMAG estabelece.

- Uma referência ao artigo [Inacessibilidade dos CAPTCHAs (W3C)](https://www.w3.org/TR/turingtest/) foi adicionada. Além disso, essa referência foi mencionada no texto da própria descrição, como leitura complementar e forma de se aprofundar mais na complexidade e nuances da discussão.

- Referência ao [Critério de Sucesso 3.3.8 Autenticação Acessível (Mínimo)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-minimum) e ao [Critério de Sucesso 3.3.9 Autenticação Acessível (Melhorado)](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#accessible-authentication-enhanced) foi adicionada.

----------------------------------------------------------------------------

### Elementos padronizados de acessibilidade digital no Governo Federal

Para concluir a análise, em relação às orientações relacionadas aos "Elementos padronizados de acessibilidade digital no Governo Federal" do eMAG, considera-se muito difícil fazer uma avaliação adequada de defasagem. Isso porque essas diretrizes, como o próprio nome sugere, são estipuladas apenas como mecanismos de acessibilidade padronizados entre os sistemas web vinculados ao Governo Federal. Elas não são uma regra de acessibilidade em si, mas uma convenção a ser seguida pelos sistemas pertencentes a esse conjunto.

Pode até ser argumentado que algumas dessas prescrições possam engessar um tanto o design de interfaces. Mas a decisão por trás delas tem muito mais relação com um aspecto político do que técnico. Eventualmente, podem até ser encontrados exemplos de sites da esfera federal que desrespeitem alguns desses elementos padronizados, mesmo eles não estando necessariamente inacessíveis. O questionamento que fica nesse ponto é se de fato o site estaria evadindo uma norma sólida estabelecida ou se tais orientações caíram por terra na prática e se tornaram meras recomendações não compulsórias. De todo modo, esse julgamento só pode ser apropriadamente estabelecido por uma equipe técnica própria vinculada ao eMAG. Por essas razões, os itens ligados aos elementos padronizados de acessibilidade digital no Governo Federal não foram considerados para a análise. 

<!-- ======================================================================= -->