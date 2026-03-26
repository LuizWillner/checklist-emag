# Colocar aqui o conteúdo do relatório de revisão e classificação de defasagem feita do conteúdo do eMAG

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

----------------------------------------------------------------------------

### 5 Multimídia

#### 5.1 Fornecer alternativa para vídeo

----------------------------------------------------------------------------

#### 5.2 Fornecer alternativa para áudio

----------------------------------------------------------------------------

#### 5.3 Oferecer audiodescrição para vídeo pré-gravado

----------------------------------------------------------------------------

#### 5.4 Fornecer controle de áudio para som

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

----------------------------------------------------------------------------

#### 6.2 Associar etiquetas aos seus campos

----------------------------------------------------------------------------

#### 6.3 Estabelecer uma ordem lógica de navegação

----------------------------------------------------------------------------

#### 6.4 Não provocar automaticamente alteração no contexto

----------------------------------------------------------------------------

#### 6.5 Fornecer instruções para entrada de dados

----------------------------------------------------------------------------

#### 6.6 Identificar e descrever erros de entrada de dados e confirmar o envio das informações

----------------------------------------------------------------------------

#### 6.7 Agrupar campos de formulário

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

### 7 Elementos padronizados de acessibilidade digital no Governo Federal

<!-- ======================================================================= -->