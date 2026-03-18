# Colocar aqui o conteúdo do relatório de revisão e classificação de defasagem feita do conteúdo do eMAG

<!-- ======================================================================= -->

### 1 Marcação

#### 1.1 Respeitar os Padrões Web

#### 1.2 Organizar o código HTML de forma lógica e semântica

#### 1.3 Utilizar corretamente os níveis de cabeçalho

#### 1.4 Ordenar de forma lógica e intuitiva a leitura e tabulação

**Defasagem do eMAG: nível nulo.**  *[TODO: Validar com Rebeca se ela entende se colocar o menu antes do conteúdo principal é obrigatório ou sugerido apenas]*

A recomendação permanece consistente com orientações de acessibilidade atuais. Porém, algumas adaptações foram feitas, no intuito de clarificar e contextualizar mais a interpretação dos seguintes aspectos do texto original:

- No quarto critério de verificação, foi incorporado mais detalhes sobre o uso do atributo `tabindex` para evitar valores maiores que 0 atribuídos, e tomar cuidado caso esses valores sejam utilizados. Em outras palavras, seu uso não foi proibido (afinal, o eMAG e o WCAG não o proíbem), apenas foi melhor explicado o que seria usar o `tabindex` com cuidado, conforme explicado pela [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Reference/Global_attributes/tabindex). Essa referência sobre o uso de `tabindex`, que ainda justifica a orientação de evitar os valores maiores que 0, também foi adicionada.

- O 3º critério de recomendação, sobre colocar no código-fonte o menu depois do conteúdo principal, foi removido. Isso porque o termo "é recomendável" antes de mencionar isso no eMAG sugere isso como algo opcional, apesar de haver uma justificativa plausível para isso *[TODO: VALIDAR COM REBECA]*. Uma discussão sobre essa questão foi movida para o exemplo de aplicação, conforme tratado no item abaixo.

- O exemplo de aplicação do eMAG foi modernizado para usar elementos HTML semanticamente mais adequados. Além disso, uma discussão sobre a implementação no código do menu de navegação antes/depois do conteúdo principal da página foi acrescentada. O eMAG sugere que esses menus sejam colocados depois e apresenta uma justificativa válida para tal, mas não parece obrigar isso *[TODO: VALIDAR COM REBECA]*.

#### 1.5 Fornecer âncoras para ir direto a um bloco de conteúdo

**Defasagem do eMAG: nível crítico.**  *[TODO: Validar com Rebea se devo ou não citar a evitação do uso de `accesskey`]*

Apesar da ideia central da orientação ser válida, o eMAG está bem defasado em relação a essa recomendação, conforme discutido a seguir.

Em primeiro lugar, a recomendação do uso do atributo `name` junto ao `id` no elemento `<a>` não é válido. Isso porque o atributo `name` é obsoleto nesse elemento e seu uso é desencorajado, conforme a [especificação do HTML Living Standard](https://html.spec.whatwg.org/multipage/obsolete.html#obsolete-but-conforming-features).

Em segundo lugar, o uso do elemento `<a>` como pontos alvo de ancoragem também é uma parece ser uma prática defasada. Tanto o [WCAG na técnica G23](https://www.w3.org/WAI/WCAG22/Techniques/general/G123#:~:text=Example%204%3A%20HTML%20page%20with%20several%20blocks%20of%20navigation) quanto o [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/a#skip_links) sugerem exemplos em que o link aponta diretamente para um outro elemento com o id especificado, e não para uma outra âncora `<a>`.

Além disso, o uso do atributo `accesskey` para atalhos de teclado é potencialmente problemático. No eMAG, ele é mencionado apenas como sugestão, mas, atualmente, seu uso é desencorajada, pois pode conflitar com outros atalhos do sistema operacional e de tecnologias assistivas, como dito no [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/accesskey#accessibility_concerns). O WCAG, principal referência de acessibilidade, nada fala sobre o uso ou não do `accesskey`

Portanto, as seguintes refatorações foram feitas:

- Desconsiderar uso do atributo `name` no elemento `<a>`, pois ele não é mais suportado nesse elemento. O exemplo em que `name` e `id` são usados serã colocado como uma má prática a ser evitada.

- Desconsiderar o uso do elemento `<a>` como pontos alvo de ancoragem (e portanto, também as técnicas citadas para esconder esses pontos de ancoragem). Seu uso só aparecerá na má prática usada para ilustrar o uso de `name` e `id`.

- *[TODO: VALIDAR COM REBECA]* Não citar o uso do `accesskey`. Esse me deixou com um pouco de dúvida. A ideia era que, como o eMAG só sugeria isso, sem necessariamente obrigar, eu omitiria a informação. Por outro lado, O MDN, não recomenda seu uso, citando justamente problemas de acessibilidade, o que me faz ter dúvidas se deveria incluir uma sugestão para não ser usado ou usado com parcimônia. O WCAG, principal referência no quesito acessibilidade, nada fala sobre o `accesskey`.

#### 1.6 Não utilizar tabelas para diagramação

#### 1.7 Separar links adjacentes

#### 1.8 Dividir as áreas de informação

#### 1.9 Não abrir novas instâncias sem a solicitação do usuário

<!-- ======================================================================= -->

### 2 Comportamento (DOM)


#### 2.1 Disponibilizar todas as funções da página via teclado

#### 2.2 Garantir que os objetos programáveis sejam acessíveis

#### 2.3 Não criar páginas com atualização automática periódica

#### 2.4 Não utilizar redirecionamento automático de páginas

#### 2.5 Fornecer alternativa para modificar limite de tempo

#### 2.6 Não incluir situações com intermitência de tela

#### 2.7 Assegurar o controle do usuário sobre as alterações temporais do conteúdo

**Defasagem do eMAG: nível nulo**  *[TODO: NECESSITA DE REVISÃO]*

Assim como o item anterior, esse item também gera uma discussão ao classificar sua defasagem. Mais uma vez, o eMAG é aqui mais restritivo que o WCAG: enquanto o eMAG chega a PROIBIR que os conteúdos animados ou em movimento disparem automaticamente, o WCAG, por outro lado, não faz essa restrição, assume a existência deles e só exige que seja possível pausar, parar ou ocultar.

À primeira vista, isso poderia ser uma defasagem leve ou moderada. Mas a abordagem mais restritiva do eMAG parece ser mais uma decisão deliberada de seus autores do que uma orientação ultrapassada, tendo em vista especialmente que o WCAG 2.0, documento em que o eMAG se baseou, já estabelecia essas diretrizes mais permissivas, e mesmo assim o eMAG adotou um caminho mais restritivo.

Em luz dessa discussão, a defasagem foi classificada como nula.

Portanto:
- Manteve-se a essência da recomendação, reescrevendo o texto apenas para que seja mais enxuto na descrição do item no checklist
- *[TODO: IDEIA PRELIMINAR A DEPENDER DA DISCUSSÃO ABAIXO]* Um exemplo utilizando `prefers-reduced-motion` como prática moderna pode ser adotado (https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion).

==================

*[TODO: VALIDAR COM REBECA]*

*Essa análise precisa ser revisada. O item 5.5 do eMAG parece estabelecer uma relação de contradição e até de redundância em certos aspectos quando comparados com esta recomendação. Além disso, revisitando o texto do eMAG, se lermos a Recomendação 2.7 com uma "lupa", a frase diz: "não devem ser disparadas automaticamente **sem o controle do usuário**". O termo "sem o controle do usuário" pode não ser uma mera redundância reforçando o termo "disparadas automaticamentes", e sim uma restrição: a proibição aqui pode não ser estritamente sobre o disparo automático em si, mas sobre o **disparo automático que não oferece uma forma de controle**. Ou seja, se o conteúdo iniciar sozinho, o usuário já deve ter à disposição imediata uma forma de pará-lo.*

*Veja mais detalhes da discussão e possibilidades de resolver esse conflito nas notas de inspeção do item 5.5.*


<!-- ======================================================================= -->

### 3 Conteúdo/Informação

#### 3.1 Identificar o idioma principal da página

#### 3.2 Informar mudança de idioma no conteúdo

#### 3.3 Oferecer um título descritivo e informativo à página

#### 3.4 Informar o usuário sobre sua localização na página

#### 3.5 Descrever links clara e sucintamente

#### 3.6 Fornecer alternativa em texto para as imagens do sítio

#### 3.7 Utilizar mapas de imagem de forma acessível

#### 3.8 Disponibilizar documentos em formatos acessíveis

**Defasagem do eMAG: nível ??**  *[TODO: Classificar defasagem]*

Esse talvez seja um dos itens mais difíceis de analisar a defasagem pelo fato de não haver um Critério de Sucesso do WCAG que seja indicado como fonte ou inspiração. O epicentro da dificuldade está na orientação:

> "Se um arquivo for disponibilizado em PDF, deverá ser fornecida uma alternativa em HTML ou ODF"

É possível conjecturar possíveis razões para ela:

1) Historicamente, o formato PDF apresentava sérios problemas em termos de acessibilidade, que só passaram a ser endereçados com a norma [ISO 14289-1 (PDF/UA)](https://pdfa.org/resource/iso-14289-pdfua) em 2012. O próprio WCAG, inclusive, enumera uma série de [técnicas para tornar documentos em PDF acessíveis](https://www.w3.org/WAI/WCAG21/Techniques/#pdf). No entanto, mesmo assim, ainda é extremamente comum encontrar PDFs inacessíveis, por uma série de razões. Talvez na época de redação do eMAG 3.1 (2014), a acessibilidade do PDF ainda não estava tão consolidada, e os autores julgaram ser melhor requerer que formatos alternativos acessíveis fossem disponibilizados.

2) Outro ponto da discussão passa pelo fato do PDF só ter sido elevado a um padrão aberto em 2008. O ODF, por definição, desde sempre foi um padrão aberto (assim como o HTML). Historicamente, há uma tendência de instituições governamentais preferirem padrões abertos e softwares livres como forma de garantir mais autonomia e segurança em governança eletrônica (algo estabelecido inclusive no [Padrões de Interoperabilidade de Governo Eletrônico - ePING](https://eping.governoeletronico.gov.br/), e talvez por isso a recomendação siga a linha dos formatos alternativos.

No entanto, o fato é que hoje o PDF é um padrão aberto e com suporte a acessibilidade, o que levanta um ponto em relação a defasagem do eMAG. Pode até ser discutível se a acessibilidade de documentos HTML e ODF é mais fácil de ser garantida. Alguns sites governamentais, como o [Government Digital Service do Reino Unido](https://www.gov.uk/guidance/publishing-accessible-documents), o [Section 508 dos EUA](https://www.section508.gov/create/pdfs/) e o [Web Accessibility Guide da Nova Zelândia](https://govtnz.github.io/web-a11y-guidance/wct/pdf-and-office-documents/publishing-pdf-and-office-documents.html) ainda especificam que haja preferência por HTML em detrimento do PDF.

Ainda assim, há exemplos de publicações de documentos em PDF do GOV.BR que não possuem alternativa em HTML ou ODF (por exemplo, alguns [editais do CPNU](https://www.gov.br/gestao/pt-br/concursonacional/editais), e fica difícil dizer se essa recomendação deixou de ser adotada oficialmente ou se esses são de fato erros de acessibilidade. O grande cerne da questão portanto é: disponibilizar  um documento somente no formato PDF, porém garantindo a sua acessibilidade, seria suficiente para cumprir essa recomendação? A sugestão de formatos alternativos é uma necessidade na visão do eMAG ou apenas uma padronização?

#### 3.9 Em tabelas, utilizar títulos e resumos de forma apropriada

#### 3.10 Associar células de dados às células de cabeçalho

#### 3.11 Garantir a leitura e compreensão das informações

#### 3.12 Disponibilizar uma explicação para siglas, abreviaturas e palavras incomuns


<!-- ======================================================================= -->

### 4 Apresentação/Design

#### 4.1 Oferecer contraste mínimo entre plano de fundo e primeiro plano

**Defasagem do eMAG: nível leve**  *[TODO: Validar com Rebeca - Há mesmo defasagem ou não na questão do contraste restritivo? Se houver, devo alterar?]*

A recomendação permanece tecnicamente válida e alinhada ao critério 1.4.3 do WCAG. Contudo, o eMAG adota uma abordagem que parece ser deliberadamente simplificada ao exigir contraste mínimo de 4,5:1 para todos os casos e ao desaconselhar o uso de imagens de fundo atrás do texto.

O WCAG 2.0 da época, por exemplo, flexibiliza o contraste mínimo para 3:1 em alguns cenários especiais no [Critério de sucesso 1.4.3: Contraste Mínimo](https://www.w3.org/TR/WCAG20/#visual-audio-contrast). Além disso, também não proibi o uso de imagens como fundo, apenas orienta que o fundo (seja uma imagem ou não) atenda o contraste mínimo ([Técnica G18](https://www.w3.org/TR/2016/NOTE-WCAG20-TECHS-20161007/G18)). Ele inclusive chega a citar que o fundo pode ser sombreado para atender o contraste mínimo, sugerindo indiretamente o uso de CSS para esse objetivo.

Essas decisões provavelmente refletem uma estratégia de padronização e simplificação da auditoria de acessibilidade em portais governamentais. Embora atualmente existam técnicas consolidadas que permitem garantir contraste adequado mesmo com imagens de fundo, a orientação do eMAG não induz a erros técnicos, apenas restringe possibilidades de design. Assim, caracteriza-se uma defasagem leve, especialmente em função da proibiçao de imagens como fundo, mas adotou-se uma abordagem conservadora de não alterar as recomendações originais do eMAG.

É válido ainda notar que o WCAG na versão 2.1, posterior ao eMAG 3.1, apresentou em seu texto, por sua vez, um novo [Critério de Sucesso 1.4.11 Contraste Não textual](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/#non-text-contrast) que estabelece a proporção mínima de 3:1 para contraste entre alguns elementos não textuais, quase como um outro cenário excepcional à regra do contraste 4,5:1. Não só isso, como no WCAG 2.2 foi adicionado ainda um outro [Critério de Sucesso 2.4.13 Aparência do Foco](https://www.w3c.br/traducoes/wcag/wcag22-pt-BR/#focus-appearance) que também estabelece contraste mínimo de 3:1 para a borda dos elementos focáveis. No entanto, como os outros casos especiais de 3:1 não foram abordados no eMAG, provavelmente pelas razões já citadas, e também decidiu-se não atualizá-los neste checklist, extrapolou-se que também não faria sentido portar esses novos critério de sucesso.

Portanto:
- As orientações bases não foram alteradas, mesmo teoricamente com elas configurando uma leve defasagem.
- Os exemplos foram melhorados para demonstrar a aplicação das cores de fundo e primeiro plano com CSS.
- Foi deixado mais claro na descrição do item o mínimo recomendado para o contraste numa folha de alto contraste, já que isso só estava sendo especificado no exemplo de aplicação
- Um exemplo de má prática de foco com contraste insuficiente foi adicionado para que os inspetores também se atentem a esse aspecto. Esse exemplo conversa diretamente com a recomendação "Possibilitar que o elemento com foco seja visualmente evidente" e seus respectivos exemplos

#### 4.2 Não utilizar apenas cor ou outras características sensoriais para diferenciar elementos

#### 4.3 Permitir redimensionamento sem perda de funcionalidade

**Defasagem do eMAG: nível leve**  *[TODO: Validar com Rebeca]*

No eMAG, essa recomendação referencia o [Critério de sucesso 1.4.4: Redimensionar Texto do WCAG 2.0](https://www.w3.org/TR/WCAG20/#visual-audio-contrast-scale). Esse critério do WCAG trata particularmente do redimensionamento de **texto**, sem perda de funcionalidade e conteúdo, em até 200%. O eMAG, por sua vez, extrapola o redimensionamento não só para o texto, mas para os elementos da página em geral.

A questão é que, na época de redação do eMAG, o WCAG 2.0 parecia só abordar o redimensionamento de texto, de maneira mais específica. No entanto, com o lançamento da versão WCAG 2.1, um novo [Critério de Sucesso 1.4.10 Realinhar](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/#reflow) foi incluído como forma de complementar mais a discussão em torno do redimensionamento abordando elementos de maneira geral da página (similar ao que o eMAG discutia). O ponto é que, de acordo com esse critério, o limite superior do zoom para manutenção de informação, funcionalidade e sem rolagem horizontal (esse último com algumas exceções) é de 400%, o dobro do que o eMAG estipulava.

O fato estranho é que, por mais que os critérios 1.4.4 e o 1.4.10 tenham abordagens um pouco diferentes, o critério 1.4.10 parece uma generalização mais ampla do 1.4.4, de forma que o cumprimento 1.4.10 parece garantir (pelo menos na maioria das vezes) o cumprimento do 1.4.4. Em outras palavras, garantir a funcionalidade e a manutenção de informação da página em zoom de 400% normalmente já garante a compreensibilidade do texto dela em zoom de 200% de maneira natural.

Além disso, o critério 1.4.10 estabelece algumas exceções para elementos em que pode ocorrer o aparecimento da barra horizontal, definindo como válido para:

> "partes do conteúdo que requerem layout bidimensional para uso ou significado" 

Por exemplo:

> "imagens, mapas, diagramas, vídeos, jogos, apresentações, tabelas de dados e interfaces em que seja necessário manter barras de ferramentas à vista ao se manipular conteúdo".

O cumprimento à recomendação do eMAG hoje, na forma que está, pode garantir a aderência ao critério 1.4.4 do WCAG e até contribuir para fornecer boa acessibilidade para a página, mas pode falhar no critério 1.4.10. Por isso, a defasagem foi classificada como de nível moderado.

Portanto:
- *[TODO: VALIDAR COM REBECA]* O limite superior para manutenção da compreensibilidade e funcionalidade da página foi aumentado de 200% para 400%, vide o novo critério 1.4.10 do WCAG 2.1.
- *[TODO: VALIDAR COM REBECA]* Exceções para a validez do aparecimento da barra horizontal ao fazer zoom foram estabelecidas, vide o novo critério 1.4.10 do WCAG 2.1.
- Além do emprego de diferentes folhas de estilo, o uso de *media queries* do CSS foi citado como possível abordagem para garantir a responsividade da página em diferentes resoluções de tela ou zooms.
- O primeiro exemplo com imagens de um site em redimensionamento de 200% foi descartado, visto que o novo limite é 400%. *[TODO: VALIDAR COM REBECA]*
- O outro exemplo com imagem de layout responsivo foi mantido *[TODO: VALIDAR COM REBECA SE POSSO FAZER ISSO OU DEVO PEGAR UM DIFERENTE]*
- *[TODO: VALIDAR COM REBECA]* Uma nova referência ao critério de sucesso 1.4.10 foi adicionada.

#### 4.4 Possibilitar que o elemento com foco seja visualmente evidente


<!-- ======================================================================= -->

### 5 Multimídia

#### 5.1 Fornecer alternativa para vídeo

#### 5.2 Fornecer alternativa para áudio

#### 5.3 Oferecer audiodescrição para vídeo pré-gravado

#### 5.4 Fornecer controle de áudio para som

#### 5.5 Fornecer controle de animação

**Defasagem do eMAG: nível ???**  *[TODO: Classificar defasagem]*

No WCAG 2.0, o [Critério de Sucesso 2.2.2: Colocar em pausa, parar e ocultar](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-pause.html), ao qual essa recomendação referencia, é um pouco mais flexível, sobretudo ao estabelecer um limite superior aceitável de 5 segundos para animações. O eMAG, por usa vez, adota uma postura mais rígida de exigir controle para "qualquer animação", mas que parece ser uma escolha deliberada, tendo em vista que as orientações do WCAG 2.0 já eram disponíveis na época de redação do eMAG. Por isso, esse aspecto não foi considerado uma defasagem.

Quanto ao exemplo com o gif, não fica claro como foi a implementação do mecanismo de pausa da animação, uma vez que o elemento `<img>` renderizando um arquivo .gif não possui um mecanismo nativo para ser pausado ou iniciado (INCLUIR REFERÊNCIA). Mesmo assim, o exemplo cumpre o propósito de ilustrar a orientação da recomendação, mesmo que não se preocupe com detalhes de implementação.

O real problema dessa recomendação é que ela parece contradizer a recomendação 2.7 "Assegurar o controle do usuário sobre as alterações temporais do conteúdo". Na recomendação 2.7, é dito que:

> "Conteúdos como slideshows, que 'se movem', rolagens, movimentações em geral ou animações não devem ser disparadas automaticamente sem o controle do usuário, mesmo em propagandas na página".

Já a atual recomendação 5.5 afirma que:

> "para qualquer animação que inicie automaticamente na página devem ser fornecidos mecanismos para que o usuário possa pausar, parar ou ocultar tal animação"

Como se ela assumisse a possibilidade de existirem animações iniciadas automaticamente, algo proibido pela anterior. Além disso, a própria recomendação 2.7 também inclui que:

> "o usuário deve ser capaz de parar e reiniciar conteúdos que se movem, sem exceção"

Englobando justamente a orientação da recomendação 5.5 e tornando-a um pouco redundante. As duas, inclusive, referenciam ao mesmo Critério de Sucesso 2.2.2.

*[TODO: VALIDAR COM REBECA]*

*Não sei bem como resolver esse dilema. A princípio, pensei nas seguintes alternativas:*

1) *Tratar a recomendação 2.7 como animações em gerais, proibindo o início automático, e a 5.5 como "animações de mídia" (vide o título da categoria), o que basicamente incluem os gifs (não consigo pensar em nenhum outro elemento), permitindo o início automático e requerendo apenas que haja controle da animação. Assim, as 2 recomendações acabam por abordar elementos ligeiramente diferentes.*

2) *Manter a redundância. Basicamente, um sistema que implemente uma animação que se inicia automaticamente, mas possui controles de parar e iniciar a animação, NÃO está aderente à recomendação 2.7, mas está conforme à recomendação 5.5. Estando conforme à 2.7, automaticamente portanto estaria conforme à 5.5. Dessa forma, a redundância existe e a divergência entre elas serviria como um mecanismo de estabelecer diferentes níveis de aderência.*

3) *(Mais radical) Remover essa recomendação e manter somente a 2.7. A princípio não é minha preferência por trazer uma alteração drástica à estrutura do eMAG, mas resolveria a redundância*

4) *Há uma possível interpretação para a recomendação 2.7 que pode alterar o significado que interpretei originalmente. Se lermos essa recomendação com uma "lupa", a frase diz: "não devem ser disparadas automaticamente sem o controle do usuári". A proibição aqui não é estritamente sobre o disparo automático em si, mas sobre o **disparo automático que não oferece uma forma de controle**. Ou seja, se o conteúdo iniciar sozinho, o usuário já deve ter à disposição imediata uma forma de pará-lo. Dessa forma, uma maneira seria tornar o início automático de animações, antes proibido estritamente, como permitido desde que haja controle disponível para o usuário. As 2 recomendações então poderiam ser mantidas como redundantes, ou adotar a estratégia 1 e 3 citadas em conjunto com esta.*

<!-- ======================================================================= -->

### 6 Formulários

#### 6.1 Fornecer alternativa em texto para os botões de imagem de formulários

#### 6.2 Associar etiquetas aos seus campos

#### 6.3 Estabelecer uma ordem lógica de navegação

#### 6.4 Não provocar automaticamente alteração no contexto

#### 6.5 Fornecer instruções para entrada de dados

#### 6.6 Identificar e descrever erros de entrada de dados e confirmar o envio das informações

#### 6.7 Agrupar campos de formulário

#### 6.8 Fornecer estratégias de segurança específicas ao invés de CAPTCHA


<!-- ======================================================================= -->

### 7 Elementos padronizados de acessibilidade digital no Governo Federal

<!-- ======================================================================= -->