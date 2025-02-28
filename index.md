<style>
  section {
    background: #fff url(./img/background.png) no-repeat center center;
    background-size: cover;
  }

  section.center img {
    display: block;
    margin: auto;
  }

  img[alt=small-img] {
    display: block;
    margin: auto;
    width: 30%;
  }

  .transparent {
    background-color: transparent!important;
  }

  section.transparent img {
    background-color: transparent!important;
  }

  section.ttable table {
    margin: auto;
  }

  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }

  .conteudo {
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }

  .conteudo-absoluto {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
  
  .large {
    font-size: 36px;
  }

  .normal {
    font-size: 22px;
  }
  .regular {
    font-size: 18px;
  }
  .small {
    font-size: 16px;
  }
  .footnotesize {
    font-size: 14px;
  }
  .scriptsize {
    font-size: 12px;
  }
  .tiny {
    font-size: 10px;
  }
  .bold {
    font-weight: bold;
  }
  .center {
    text-align: center;
  }
  section.lead p {
    text-align: justify;
  }
  section.lead h1 {
    text-align: center;
  }
  section.lead h2 {
    text-align: center;
  }
  section.lead h3 {
    text-align: center;
  }
  
  .grid-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: justify;
  }

  .grid-25-25-25-25 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    text-align: justify;
  }

  .grid-33-33-33 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: justify;
  }


  .grid-66-33 {
    display: grid;
    grid-template-columns: 2fr 1fr;
    text-align: justify;
  }

  .grid-33-66 {
    display: grid;
    grid-template-columns: 1fr 2fr;
    text-align: justify;
  }

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
  }
  img[alt=grid-img] {
    width: 100%;
  }
  img[alt=slide-img] {
    width: 75%;
  }


</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>


# Análise de Circuitos Elétricos
## Aula 08 - Análise do Regime Permanente Senoidal
 
Prof. M.Sc. Diego Ascânio Santos (ascanio@cefetmg.br)

Aula baseada sobre o material do professor Dr. Emerson Gonçalves de Melo (emerdemelo@usp.br - DEMAR EEL USP), da professora Drª. Thabatta Moreira Alves de Araújo (thabatta@cefetmg.br - DIGDDV), da Khan Academy e da bibliografia padrão da disciplina.

CEFET-MG DIGDDV - Divinópolis, 2023.


---

## Roteiro

1. Fonte senoidal. 
2. Resposta senoidal.
3. O conceito de Fasor
4. Elementos passivos no domínio da frequência.
5. As leis de Kirchhoff no domínio da frequência.
6. Associações em série e em paralelo e transformações \\(\Delta\\) - Y.
7. Equivalentes de Thévenin e de Norton.
8. Transformadores.
9. Diagramas fasoriais.


---

## Objetivos

<div class="normal">

1. Entender o conceito de fasor e saber realizar uma transformada fasorial e a transformada inversa.
2. Saber transformar um circuito alimentado por uma fonte senoidal para o domínio da frequência através do conceito de fasor.
3. Saber aplicar as seguintes técnicas de análise de circuitos no domínio da frequência:
    1. Leis de Kirchhoff.
    2. Associação de elementos em série, paralelo e transformação delta-estrela.
    3. Divisão de tensão e corrente.
    4. Equivalentes de Thévenin e Norton.
4. Saber analisar circuitos que contenham transformadores lineares usando métodos fasoriais.
5. Entender as relações terminais do transformador ideal e saber analisar circuitos que contenham transformadores ideiais usando métodos fasoriais.

</div>


---

## Contextualização

Até o momento trabalhamos apenas com circuitos contínuos alimentados por fontes de tensão ou de corrente.

Agora, vamos estudar circuitos energizados por fontes de tensão (ou corrente) que variem com o tempo — também conhecidos como **circuitos de corrente alternada (CA)**.

As fontes objetos do nosso estudo são aquelas que fornecem tensões / correntes que variam de forma senoidal em relação ao tempo.


---

## Contextualização

<div class="normal">

Por que é importante estudarmos correntes alternadas?

- Geração, transmissão, distribuição e consumo de energia elétrica nas aplicações cotidianas — energia elétrica industrial, comercial, residencial — acontecem em condições de regime permanente (tensões e correntes) caracterizadas por funções senoidais alternadas, que variam com o tempo.

- O entendimento do regime senoidal possibilita a previsão do comportamento de sistemas com fontes não senoidais (transformadas de Fourier permitem aproximar quaisquer funções em termos de senoides).

- O regime senoidal simplifica o projeto de sistemas elétricos — um projetista de sistemas elétricos pode formular seus circuitos em termos de uma resposta de um regime permanente senoidal desejável e projetar os circuitos para satisfazer tais características. Se os projetos funcionarem no regime permanente senoidal, eles funcionarão em qualquer regime.

</div>


---

## Aplicação prática do regime permanente senoidal
### Circuito de distribuição residencial de energia elétrica

<div class="grid-50-50">

<div class="grid-element regular">

</div>

<div class="grid-element regular">

</div>


</div>


---

<!-- _class: lead -->
# 1. Fonte senoidal


---

## 1. Fonte senoidal

<div class="grid-50-50 regular">

<div class="grid-element">

Uma fonte de tensão (corrente) senoidal gera uma tensão (corrente) que oscila em um padrão senoidal com o tempo.

<div class="footnotesize">

As análises que realizaremos são inicialmente focadas para fontes de tensão seinoidais, porém, suas conclusões são igualmente estendidas para fontes de corrente senoidais.

</div>

- Funções que variam senoidalmente podem ser expressas por meio de senos ou cossenos.
- Ambas funcionam bem, mas, não podem ser utilizadas ao mesmo tempo.
- Em nossas análises será utilizada a função cosseno e, consequentemente, a fonte de tensão senoidal será expressa por:

\\[
    v = V_{m} \cos({\omega t + \phi})
\\]

- O gráfico desta função é representado pela figura 2.

</div>

<div class="grid-element">

<figure>

<!-- _class: transparent center -->
![grid-img](https://i.imgur.com/aqyAWJd.png)

<div class="footnotesize center">

<figcaption>

Figura 2 - Gráfico da função \\(v = V_{m} \cos({\omega t + \phi})\\)

</figcaption>

</div>

</figure>

</div>

</div>


---

## 1. Fonte senoidal

<div class="grid-50-50 regular">

<div class="grid-element">

Analisando a figura 2, podemos perceber que a função senoidal repete-se por intervalos regulares. Esta característica representa a periodiciade da função senoidal e por isso, esta função também é denominada periódica.

Para os objetivos de nosso estudo, é importante entendermos o intervalo de tempo que a função senoidal leva para atingir todos os seus valores possíveis e, então, começar uma nova repetição destes valores. Este intervalo é denominado período e é representado pela letra <span class="big"> **\\(T\\)** </span>, sendo medido em segundos.

A grandeza recíproca (inversa) a \\(T\\) é denominada frequência e é representada pela letra <span class="big"> **\\(f\\)** </span>, sendo medida em Hertz (Hz). A frequência representa a quantidade de vezes (número de ciclos) por segundo que a função senoidal se repete.

\\[
f = \frac{1}{T}
\\]

</div>

<div class="grid-element">

<figure>

<!-- _class: transparent center -->
![grid-img](https://i.imgur.com/aqyAWJd.png)

<div class="footnotesize center">

<figcaption>

Figura 2 - Gráfico da função \\(v = V_{m} \cos({\omega t + \phi})\\)

</figcaption>

</div>

</figure>

</div>

</div>


---

## 1. Fonte senoidal - Características da Equação da Tensão

<div class="grid-50-50 regular">

<div class="grid-element">

Consideremos novamente a equação que descreve a tensão:

\\[
    v = V_{m} \cos({\omega t + \phi})
\\]

O coeficiente \\(\omega\\) de \\(t\\) contém necessariamente o valor numérico de \\(f\\) — \\(\frac{1}{T}\\) — e é chamado de **frequência angular** da função senoidal, sendo expresso por:

\\[
    \omega = 2 \pi f = \frac{2 \pi}{T} (\frac{\text{radianos}}{\text{segundo}}) \tag{1}
\\]

A cada vez que a função cosseno (ou seno) passa por um conjunto completo de seus valores, seu argumento \\(\omega t \\) percorre \\(2 \pi\\) rad \\((360 °)\\) e é este fato que embasa a definição de frequência angular (na equação 1).

Podemos concluir também que todas as vezes que \\(t\\) for um múltiplo de \\(T\\), \\(\omega t\\) será múltiplo inteiro de \\(2 \pi\\) rad.

</div>

<div class="grid-element">

O coeficiente \\(V_{m}\\) é a **amplitude máxima** da tensão senoidal. Como \\(\pm 1\\) são os valores extremos do cosseno, \\(\pm V_{m}\\) limita a amplitude da tensão senoidal.

O ângulo \\(\phi\\) da equação que descreve a tensão é chamado de **ângulo de fase** da tensão senoidal. Ele determina o valor da função senoidal no instante \\(t = 0\\); portanto, fixa o ponto da onda periódica em que começamos a medir o tempo. A alteração do ângulo de fase \\(\phi\\) provoca um deslocamento da onda senoidal ao longo do eixo do tempo, mas, não exerce nenhum efeito sobre a amplitude \\(V_{m}\\) ou sobre a frequência angular \\(\omega\\), como mostra a figura 3:

<figure class="center">

<div class="tiny">

<!-- _class: transparent center -->
![](https://i.imgur.com/wW8pzia.png)

<figcaption> Figura 3 - Deslocamento da onda senoidal ao longo do eixo do tempo quando <span>

 \\(\phi = 0\\) 

</span> </figcaption>

</div>

</figure>

</div>

</div>


---

## 1. Fonte senoidal - Características da Equação da Tensão

<div class="grid-50-50 scriptsize">

<div class="grid-element">

<figure class="center">

<div class="tiny">

<!-- _class: transparent center -->
![](https://i.imgur.com/wW8pzia.png)

<figcaption> Figura 3 - Deslocamento da onda senoidal ao longo do eixo do tempo quando <span>

 \\(\phi = 0\\) 

</span> </figcaption>

</div>

</figure>

Ainda observando a figura 3, as seguintes observações têm de ser feitas:

1. Definir \\(\phi = 0\\) na função \\(v = V_{m} \cos(\omega t + \phi)\\) desloca a onda \\(\frac{\phi}{\omega}\\) unidades de tempo para a direita.
2. Quando \\(\phi > 0\\), a onda senoidal desloca-se para a esquerda.
3. Quando \\(\phi < 0\\), a onda senoidal desloca-se para a direita.

</div>

<div class="grid-element">

4. \\(\phi\\) e \\(\omega t\\) devem ter as mesmas unidades, pois, são argumentos da função cossenoidal.
    1. Se \\(\omega t\\) for expressa em radianos (graus), espera-se que \\(\phi\\) também seja.
    2. Quando os dois ângulos forem expressos em unidades distintas, é necessário fazer a conversão de um deles para a unidade do outro, que pode ser realizada pela seguinte fórmula:
        - \\(\text{número de graus} = \frac{180°}{\pi} (\text{número de radianos})\\)

Retornando à função da tensão, expressa por \\(v = V_{m} \cos(\omega t + \phi)\\), outra característica de suma importância obtida de sua constituição é o seu **valor eficaz** ou **rms**, uma medida que representa a equivalência da tensão senoidal em termos de potência com uma tensão contínua. 

<!-- O Valor eficaz é útil porque possibilita calcular a potência dissipada por uma carga como se tal carga estivesse submetida a uma tensão contínua (facilitando o projeto de sistemas elétricos). -->

O valor eficaz é definido pela raiz quadrada do valor médido da função ao quadradado. Daí, se \\(f = V_{m} \cos({\omega t + \phi})\\), logo, \\(V_{rms}\\) é dado por:

\\[
\begin{align}
    V_{rms} &= \sqrt{\frac{1}{T + T_{0} - T_{0}} \int_{T_{0}}^{T + T_{0}}|f(t)|^{2} dt} \therefore \tag{2} \\\\
    V_{rms} &= \sqrt{\frac{1}{T} \int_{T_{0}}^{T + T_{0}}{{V_{m}}^{2}{\cos^{2}({\omega t + \phi})} dt}} \therefore \\\\
    V_{rms} &= \frac{V_{m}}{\sqrt{2}}
\end{align}
\\]

<!-- 
Com isso, verificamos que o valor eficaz de uma tensão senoidal depende somente da amplitude da tensão e não do ângulo de fase (ou da sua frequência)

Assim, qualquer sinal senoidal pode ser compleamente descrito se conhecermos sua frequência, seu ângulo de fase e sua amplitude (ou o valor máximo ou o valor eficaz)
-->

</div>

</div>


---

<!-- _class: lead -->

# Exemplos de fontes senoidais 9.1, 9.2, 9.3 e 9.4


---

## Exemplos 9.1, 9.2, 9.3 e 9.4 (NILSSON; RIEDEL 10ª Ed)

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplos_9.1_9.2_9.3_9.4.ipynb" width=100% height=100%></iframe> 


---

<!-- _class: lead -->
# Resposta Senoidal


---

## Resposta Senoidal

<div class="grid-50-50 regular">

<div class="grid-element">

Queremos mostrar através da dificuldade da obtenção da resposta senoidal pelos métodos tradicionais de resolução de EDOs a importância de se ter alternativas simplificadas que sejam capazes de resolver esse tipo de problema. No nosso caso, a representação fasorial.

Considere o circuito abaixo alimentado por uma tensão senoidal \\(v_{s} = V_{m} \cos(\omega t + \phi)\\).

<!-- _class: transparent center -->
![](https://i.imgur.com/9fiWK0d.png)

Por conveniência é considerado que \\(I(0) = 0\\) e o tempo só é contado a partir do instante em que a chave é fechada. Qual a função a resposta da corrente \\(i(t)\\) neste circuito RL?

</div>
<div class="grid-element">

Sabemos pela LKT nas malhas:

\\[
\begin{align}
v_{s} &= v_{R} + v_{L} \therefore \\\\
V_{m} \cos(\omega t + \phi) &= R i(t) + L \frac{di(t)}{dt} \therefore \\\\
L \frac{di(t)}{dt} + R i(t) &= V_{m} \cos(\omega t + \phi)
\end{align}
\\]

Não desenvolveremos a [solução da EDO](https://ava.cefetmg.br/mod/assign/view.php?id=107802), mas sim mostrar (e aceitar) que ela é dada por:

\\[
\begin{align}
    i(t) &= \frac{-V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos(\phi - \theta) e^{-(\frac{R}{L}) t} \\\\
         &+ \frac{V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos({\omega t + \phi - \theta}) \\\\
\end{align}
\\]

Onde \\(\theta\\) é o ângulo cuja tangente é \\(\frac{\omega L}{R}\\). Assim, se:
\\[
\begin{align}
    \tan{\theta} &= \frac{\omega L}{R} \therefore \\\\
    \theta &= \arctan{\frac{\omega L}{R}}
\end{align}
\\]

</div>

</div>


---

## Resposta Senoidal

<div class="small">

As seguintes observações a respeito da corrente \\(i(t) = \frac{-V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos(\phi - \theta) e^{-(\frac{R}{L}) t} + \frac{V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos({\omega t + \phi - \theta})\\) têm de ser efetuadas:

1. A expressão \\(\frac{-V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos(\phi - \theta) e^{-(\frac{R}{L}) t}\\) é denominada **componente transitória** da corrente, pois ela se torna infinitesimal (tende à zero) quando \\(t \rightarrow \infty\\).
2. Já a segunda expressão \\(\frac{V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}} \cos({\omega t + \phi - \theta})\\) é denominada **componente do regime permanente** da corrente e existirá enquanto a chave do circuito \\(RL\\) permanecer fechada.

    1. Será desenvolvida uma técnica para calcular diretamente a resposta do regime permanente (para não precisar resolver a EDO);
        - Entretanto, tal técnica não permite que a resposta do estado transitório ou a resposta total do sistema sejam obtidas de imediato;
    2. Ao analisar esta segunda expressão verifica-se que a resposta do regime permanente é uma função senoidal;
    3. Que a frequência do sinal de resposta é a mesma do sinal oriundo da fonte de tensão;
    4. De modo geral, a amplitude máxima da resposta de regime permanente é diferente da amplitude máxima da tensão oriunda da fonte.
        - Neste caso, a amplitude máxima da resposta de regime permanente é dada por \\(\frac{V_{m}}{\sqrt{R^{2} + \omega^{2} L^{2}}}\\).
        - E a amplitude máxima da tensão oriunda da fonte é dada por \\(V_{m}\\).
    5. Por fim, é costume que o ângulo de fase do sinal da resposta seja diferente do ângulo de fase da fonte.
        - Neste caso do circuito \\(RL\\), o ângulo de fase da compomenente permanente da resposta é dado por \\(\phi - \theta\\).
        - E o ângulo de fase da fonte é dado por \\(\phi\\).

Todas estas características nos ajudam a entender a motivação do **método dos fasores** — que nos ajuda a resolver as EDOs apenas pela análise da resposta do regime permanente (determinar a amplitude máxima da resposta do regime permanente e o ângulo de fase de seu sinal) quando sejam conhecidas a forma de onda e a frequência da resposta — abordado na sequência.

</div>


---

<!-- _class: lead -->
# Método dos Fasores


---

## Fasores - Método dos Fasores

O método dos fasores é um método matemático que simplifica a análise de circuitos que operam em regime permanente senoidal. Fasores, como veremos na sequência, são representações complexas de ondas senoidais, onde as magnitudes e as fases das ondas são expressas como números complexos. Estas representações permitem transformar equações diferenciais em equações algébricas, o que simplifica muito a análise de circuitos.


---

## O Conceito de Fasor

<div class="regular">

Fasor é um número complexo que contém as informações da amplitude e do ângulo de fase de uma função senoidal. Seu conceito fundamenta-se na identidade de Euler, que relaciona a função exponencial com a função trignométrica:

\\[
    e^{\pm j\theta} = \cos(\theta) \pm j\sin(\theta)
\\]

Esta equação é importante porque nos fornece outra maneira de representar as funções trignométricas cosseno e seno. Podemos expressar a função cosseno como a parte real da função exponencial complexa, e a função seno como a parte imaginária da função exponencial complexa; como visto:

\\[
\\begin{align}
    \\cos(\\theta) &= ℜ  \\left\\{ e^{j \\theta} \\right\\} \\\\
    \\sin(\\theta) &= ℑ  \\left\\{ e^{j \\theta} \\right\\}
\\end{align}
\\]

ℜ (forma alternativa da letra R) e ℑ (forma alternativa da letra I) são operadores que extraem a parte real e a parte imaginária de um número complexo significando, respectivamente, **ℜ : a parte real de** e **ℑ : a parte imaginária de**.

</div>


---

## O Conceito de Fasor

<div class="grid-50-50 regular">

<div class="grid-element">

Voltemos agora ao nosso circuito \\(RL\\) com uma fonte de tensão senoidal \\(v_{s}\\) descrita por: \\(v_{s}(t) = V_{m} \cos(\omega t + \phi)\\).

</div>

<div class="grid-element">

<!-- _class: transparent center -->
![](https://i.imgur.com/9fiWK0d.png)

</div>

</div>

<div class="regular">

Como preconizado pelo conceito da representação fasorial, podemos representar a função \\(\cos(\theta)\\) como a parte real ℜ  de um número complexo \\(e^{j\theta}\\), ou seja, \\(\cos(\theta) = ℜ\{e^{j\theta}\}\\) e podemos representar a função \\(\sin(\theta)\\) como a parte imaginária ℑ de um número complexo \\(e^{j\theta}\\), ou seja, \\(\sin(\theta) = ℑ\{e^{j\theta}\}\\).

Se \\(v_{s}(t) = V_{m} \cos(\omega t + \phi)\\), então 

\\[
\begin{align}
    v_{s}(t) &= ℜ\\\{V_{m} e^{j(\omega t + \phi)}\\} \\\\
    v_{s}(t) &= ℜ\\\{V_{m} e^{j\phi} e^{j\omega t}\\} \tag{3}
\end{align}
\\]

Quando aplicadas as devidas manipulações algébricas e trigonométricas (pag. 344 Circuitos Elétricos 10ª Ed.; NILSSON; RIEDEL).

</div>


---

## O Conceito de Fasor - Transformada Fasorial

<div class="grid-50-50 regular">

<div class="grid-element">

Continuemos nossa análise pela equação 3:

\\[
\begin{align}
    v_{s}(t) &= ℜ\\\{V_{m} e^{j\phi} e^{j\omega t}\\} \tag{3}
\end{align}
\\]

A quantidade \\(V_{m} e^{j \phi}\\) é um número complexo que contém informações sobre a amplitude e o ângulo de fase da tensão senoidal \\(V_{m} \cos(\omega t + \phi)\\). Este número complexo \\(V_{m} e^{j \phi}\\) é, por definição, a **representação do fasor** (ou, **transformada fasorial**) da função senoidal dada.

Assim, o fasor **V** é definido como:

\\[
\\begin{align}
    \\mathbf{V} &= V_{m} e^{j \\phi} = Ƒ \left\\{ V_{m} \\cos(\\omega t + \\phi) \right\\} \tag{4}
\\end{align}
\\]

Onde a notação \\(Ƒ \left\\{ V_{m} \\cos(\\omega t + \\phi) \right\\}\\) é lida como **"a transformada fasorial de \\(V_{m} \\cos(\\omega t + \\phi)\\)"**.

</div>
<div class="grid-element">

Preste bastante atenção neste conceito de **transformada fasorial**, pois, tal conceito é fundamental para a análise de circuitos em regime permanente senoidal.

O que de fato significa uma transformada fasorial? É uma função de transformação que converte funções representadas no domínio do tempo (**real**) para o domínio dos números complexos, também conhecido como **domínio da frequência**.

Como diferenciar uma variável representada no domínio do tempo de outra representada no domínio da frequência? 
- Por convenção adotamos a notação de variáveis (fasores) no domínio da frequência em negrito, como por exemplo, **V** na equação 4 e as variáveis no domínio do tempo não utilizamos destaques em seus nomes.

Porque a transformada fasorial é importante? Porque, como veremos a seguir, ela permite reduzir a análise de circuitos em regime permanente senoidal a simples operações algébricas de números complexos.

</div>

</div>


---

## O Conceito de Fasor - Transformada Fasorial

<div class="regular">

Retomemos nossa análise do fasor \\(\mathbf{V}\\) da equação 4:

\\[
\\begin{align}
    \\mathbf{V} &= V_{m} e^{j \\phi} = Ƒ \left\\{ V_{m} \\cos(\\omega t + \\phi) \right\\} \tag{4}
\\end{align}
\\]

Como vimos no slide anterior \\(Ƒ \left\\{ V_{m} \\cos(\\omega t + \\phi) \right\\} \\) é a transformada fasorial de \\(V_{m} \\cos(\\omega t + \\phi)\\).

A equação 4 — \\(\\mathbf{V} = V_{m} e^{j \\phi}\\) — é a forma polar do fasor \\(\mathbf{V}\\) (no sistema de coordenadas polares).

Também é possível expressar o fasor \\(\mathbf{V}\\) no sistema de coordenadas retangulares (ou cartesianas) como:

\\[
\\begin{align}
    \\mathbf{V} = V_{m} \\cos(\\phi) + j V_{m} \\sin(\\phi) \tag{5}
\\end{align}
\\]

E por meio da notação angular:

\\[
\\begin{align}
    \\mathbf{V} = V_{m} \\angle \\phi \equiv V_{m} e^{j \\phi} \tag{6}
\\end{align}
\\]

Todas estas notações são bastante úteis em aplicações do conceito de fasor na análise de circuitos e usaremos extensivamente a notação angular nos próximos conteúdos.

</div>


---

## O Conceito de Fasor - Transformada Fasorial Inversa

<div class="regular">

Até o momento fizemos a transformada fasorial da função senoidal \\(v_{s}(t)\\), entretanto, é possível fazer o processo inverso, transformar uma representação fasorial \\(\\mathbf{V}\\) em uma função senoidal \\(v_{s}(t)\\), ou seja, escrever para um fasor a expressão de sua funão senoidal equivalente.

Consideremos o fasor \\(\\mathbf{V} = {100} \angle {-26°} \\).

Como escolhemos usar a função cosseno como função senóide para tensão, temos que sua representação senoidal é:

\\[v_{s}(t) = 100 \cos(\omega t - 26°)\\]

Somente com as informações contidas na representação fasorial não é possível deduzir o valor de \\(\omega\\), pois, ele contém somente as informações de amplitude e de fase. A ação de converter a transformada fasorial para sua expressão no domínio do tempo é denominada de **transformada inversa fasorial** e é representada pela equação:

\\[
Ƒ^{-1} \\{ V_{m} e^{j \phi} \\} = ℜ  \left\\{ V_{m} e^{j \phi} e^{j \omega t} \right\\} \tag{7}
\\]

</div>


---

## O Conceito de Fasor - Transformada Fasorial Inversa

<div class="regular">

\\[
Ƒ^{-1} \\{ V_{m} e^{j \phi} \\} = ℜ  \left\\{ V_{m} e^{j \phi} e^{j \omega t} \right\\} \tag{7}
\\]

Estudando a equação 7, o termo a esquerda, \\(Ƒ^{-1} \\{ V_{m} e^{j \phi} \\}\\), representa a própria **transformada fasorial inversa** e o termo a direita, \\(ℜ  \left\\{ V_{m} e^{j \phi} e^{j \omega t} \right\\}\\) , indica como devemos obter a transformada fasorial a inversa, ou seja, devemos multiplicar o fasor \\(V_{m} e^{j \phi}\\) por \\(e^{j \omega t}\\) e, então, extrair a parte real do resultado.

Reiterando, a transformada fasorial é valiosa porque permite determinar a amplitude máxima e o ângulo de fase da resposta permanente senoidal pela álgebra de números complexos. As seguintes observações corroboram este fato:

</div>

<div class="regular grid-50-50" style="border: solid 2px #663399;">

<div class="grid-element">

1. A componente transitória da resposta senoidal se extingue à medida que o tempo passa. Portanto, quando \\(t \rightarrow \infty\\), a componente permanente é quem satisfaz a equação diferencial que descreve o sistema.
2. Em um circuito linear estimulado por fontes senoidais, a resposta permanente também é senoidal com a mesma frequência da fonte.

</div>

<div class="grid-element">

3. Usando a notação para \\(\cos(\theta) = ℜ \left\\{ e^{j \theta} \right\\}\\) é possível propor \\(ℜ \left\\{ A e^{j \beta} e^{j \omega t} \right\\}\\) como solução para o regime permanente do sistema, onde \\(A\\) é a amplitude máxima da resposta e \\(\beta\\) seu ângulo de fase.
4. Quando substituímos a solução de regime permanente proposta na EDO do sistema, o termo exponencial \\(e^{j \omega t}\\) se cancela, deixando a solução para \\(A\\) e \\(\beta\\) no domínio dos números complexos.

</div>

</div>


---

## Transformada Fasorial — Verificação das Observações

<div class="grid-50-50 regular">

<div class="grid-element">

Em relação as observações contidas no slide anterior, utilizaremos o circuito RL tema desta aula para verificar as observações.

</div>

<div class="grid-element">

<!-- _class: transparent center -->
![](https://i.imgur.com/9fiWK0d.png)

</div>

</div>

<div class="regular">

Pelo fato de utilizarmos uma função cossenoidal para descrever o sinal senoidal da nossa fonte de tensão, então, usamos a equação \\(\cos(\theta) = ℜ \left\\{ e^{j\theta} \right\\}\\) para fazer a transformada fasorial necessária. A grandeza de interesse (pelo exemplo do livro) é a corrente de regime permanente do circuito \\(i_{rp}(t)\\) que também é descrita por uma função senoidal do tipo cosseno, por conveniência.

Considerando este fato, bem como que a amplitude da corrente é \\(I_{m}\\), logo, a representação fasorial da corrente de regime permanente é dada por:

\\[
    i_{rp} (t) = ℜ \left\\{I_{m} e^{j \beta} e^{j \omega t} \right\\}
\\]

Ou seja, \\(i_{rp}(t)\\) é dada pela parte real de \\(\left\\{I_{m} e^{j \beta} e^{j \omega t} \right\\}\\). Quando substituimos a corrente \\(i_{rp}(t)\\) pela sua representação fasorial na equação diferencial \\(L \frac{di(t)}{dt} + R i(t) = V_{m} \cos(\omega t + \phi) \\) que descreve o circuito RL, obtemos:

\\[
    ℜ \\left\\{j \\omega L I_{m} e^{j \beta} e^{j \omega t} \\right\\} + ℜ \\left\\{R I_{m} e^{j \beta} e^{j \omega t} \\right\\} = ℜ \\left\\{V_{m} e^{j \phi} e^{j \omega t} \\right\\} \\tag{8}
\\]

</div>


---

## Transformada Fasorial — Verificação das Observações

<div class="regular">

\\[
    ℜ \\left\\{j \\omega L I_{m} e^{j \beta} e^{j \omega t} \\right\\} + ℜ \\left\\{R I_{m} e^{j \beta} e^{j \omega t} \\right\\} = ℜ \\left\\{V_{m} e^{j \phi} e^{j \omega t} \\right\\} \\tag{8}
\\]

Para deduzirmos esta equação 8, assumimos que tanto a diferenciação quanto a multiplicação por uma constante pode ser realizada na parte real de uma expressão. Também, reescrevemos o lado direito da equação 8 usando a notação fasorial que preconiza que \\(\cos(\theta) = ℜ \\left\\{e^{j \theta} \\right\\}\\).

Pela álgebra de números complexos, sabemos que a soma das partes reais de números complexos é igual à parte real da soma destes números. Portanto, é possível reduzir o lado esquerdo da equação 8 para um único termo:

\\[
    ℜ \\left\\{(j \\omega L + R)I_{m} e^{j \beta} e^{j \omega t} \\right\\} = ℜ \\left\\{ V_{m} e^{j \phi} e^{j \omega t} \\right\\} \\tag{9}
\\]

</div>


---

## Transformada Fasorial — Verificação das Observações

<div class="regular">

Porque escolhemos a função cosseno para ser nossa representação senoidal é que extraimos a parte real da função exponencial. Se tivéssemos escolhido a função seno para analisar o regime permanente senoidal, teríamos extraído a parte imaginária da função exponencial (pela notação fasorial) que preconiza que \\(\sin(\theta) = ℑ \\left\\{ e^{j \theta} \\right\\} \\). Portanto, se considerássemos a representação senoidal da corrente do regime permanente como uma função seno, nossa equação para o estado estacionário neste regime seria:

\\[
ℑ \\left\\{ (j \omega L + R) I_{m} e^{j \beta} e^{j \omega t} \\right\\} = ℑ \\left\\{ V_{m} e^{j \phi} e^{j \omega t} \\right\\} \tag{9}
\\]

Retomando agora a equação 8:

\\[
    ℜ \\left\\{j \\omega L I_{m} e^{j \beta} e^{j \omega t} \\right\\} + ℜ \\left\\{R I_{m} e^{j \beta} e^{j \omega t} \\right\\} = ℜ \\left\\{V_{m} e^{j \phi} e^{j \omega t} \\right\\} \\tag{8}
\\]

Observe que as partes complexas e reais das equações 8 e 9 são iguais. Portanto,

\\[
    (j \omega L + R)I_{m} e^{j \beta} = V_{m} e^{j \phi} \\therefore \\\\
    I_{m} e^{j \beta} = \\frac{V_{m} e^{j \phi}}{R + j \omega L} \\tag{10}
\\]

</div>




---

## Transformada Fasorial — Verificação das Observações

<div class="regular">

Na equação 10 — \\(I_{m} e^{j \beta} = \\frac{V_{m} e^{j \phi}}{R + j \omega L}\\) — Foi possível descartar \\(e^{j \omega t}\\) porque ele é comum a todos os termos da equação. Assim, para este circuito, devemos determinar as grandezas de interesse \\(I_{m}\\) e \\(\beta\\) pela manipulação algébrica das quantidades complexas \\(V_{m} e^{j \phi}\\) e \\(R + j \omega L\\). Observe que foram encontradas tanto a forma polar quanto a forma retangular.

Por fim, devemos nos atentar ao fato que a transformada fasorial, juntamente com sua inversa, permite-nos transitar entre o domínio do tempo e o domínio da frequência. Por consequência, quando obtemos uma solução, estamos ou no domínio do tempo ou no domínio da frequência, mas, nunca nos dois ao mesmo tempo, por ser impossível e absurdo.


</div>


---

## Transformada Fasorial — Verificação das Observações

<div class="regular">

Isso tudo que fizemos foi para formalizar os princípios de transformações do domínio do tempo para o domínio da frequência através de transformadas fasoriais que nos permitem a aplicação de técnicas algébricas complexas que simplificam a resolução de circuitos elétricos em regime permanente senoidal.

Assim, isto implica na aplicação do princípio da superposição (de tensões e correntes) através das representações fasoriais, o que torna válido tanto a superposição de tensões (correntes) no domínio do tempo:

\\[
    v(t) = v_{1}(t) + v_{2}(t) + \cdots + v_{n}(t) \\\\
    i(t) = i_{1}(t) + i_{2}(t) + \cdots + i_{n}(t)
\\]

Quanto no domínio da frequência:

\\[
    \textbf{V} = \textbf{\\(V_{1}\\)} + \textbf{\\(V_{2}\\)} + \cdots + \textbf{\\(V_{n}\\)} \\\\
    \textbf{I} = \textbf{\\(I_{1}\\)} + \textbf{\\(I_{2}\\)} + \cdots + \textbf{\\(I_{n}\\)}
\\]

Portanto, a representação do fasor é a soma dos fasores dos termos individuais.

Finalizado o arcabouço teórico que verifica a validade das transformadas fasoriais, veremos agora identidades trigonométricas, bem como, as operações algébricas de números complexos, que facilitam a análise dos circuitos no regime permanente senoidal.

</div>


---

## Fasores — Identidades Trigonométricas

<!-- _class: transparent center -->
![slide-img](https://i.imgur.com/shE7UKe.png)


---

## Fasores - Números Complexos e relações entre formas retangulares e fasoriais

<div class="regular">

### Números Complexos — Pequena Revisão

- ℂ é o conjunto dos números complexos, mais abrangente que o dos números reais (ℝ).
- Compreendem valores compostos por uma parte real e uma parte imaginária (que representa raízes de números negativos: \\( i = \sqrt{-1} \\)).
- Na engenharia elétrica e afins utilizamos a notação \\(j\\) para representar a parte imaginária, pois \\(i\\) é geralemente utilizada para representar a corrente elétrica.

<!-- _class: transparent center -->
![](https://i.imgur.com/TlU0ZlE.png)

</div>


---

## Fasores - Operações Matemáticas sobre Números Complexos

<div class="regular">

Considerando \\(z_{1} = x_{1} + jy_{1}\\) e \\(z_{2} = x_{2} + jy_{2}\\):

<!-- _class: transparent center -->
![](https://i.imgur.com/mXrrDzU.png)

</div>


---

## Fasores - Pequena tabela para conversão entre representações no domínio do tempo e no domínio da frequência

<!-- _class: transparent center -->
![](https://i.imgur.com/Vn5pbmi.png)


---

## Fasores - Relação entre integral e derivada no domínio do tempo e no domínio da frequência

<!-- _class: transparent center -->
![](https://i.imgur.com/SMAeXxV.png)


---

<!-- _class: lead -->
# Exemplo 9.5

## Soma de cossenos usando-se fasores.

Se \\(y_{1} = 20 \cos(\omega t - 30°) \text{ e } y_{2} = 40 \cos(\omega t + 60°)\\) expresse \\(y = y_{1} + y_{2}\\) como uma única função senoidal.

a) Resolva o problema usando identidades trigonométricas.

b) Resolva o problema usando o conceito de fasor.


---

<!-- _class: lead -->
## Soma de cossenos usando-se fasores

<center>
<iframe width="727" height="409" src="https://www.youtube.com/embed/fbPHS42Dc8A" title="Me Salva! SEN07 - Soma Fasorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</center>
