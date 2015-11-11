---
title: "Instrução"
bg: white
color: black
style: center
---
{::options parse_block_html="true" /}

### Vehicle Routing Problem
{: .text-orange}

# Problema de Roteamento de Veículos
{: .text-orange}


<p style="font-size: 0;">
    <span class="fa-stack subtlecircle hidden-mobile" style="font-size: 50px; background: white">
      <i class="fa fa-circle fa-stack-2x text-white"></i>
      <i class="fa fa-building-o fa-stack-1x text-orange"></i>
    </span>

    <span class="fa-stack subtlecircle" style="font-size:100px; background: white;margin: 0 25px;">
      <i class="fa fa-circle fa-stack-2x text-white"></i>
      <i class="fa fa-car fa-stack-1x text-orange"></i>
    </span>

    <span class="fa-stack subtlecircle hidden-mobile" style="font-size: 50px; background: white">
      <i class="fa fa-circle fa-stack-2x text-white"></i>
      <i class="fa fa-home fa-stack-1x text-orange"></i>
    </span>
</p>

<br>

O **Problema de Roteamento de Veículos** (*Vehicle Routing Problem* ou *VRP*) foi introduzido em 1959 por [**Dantzig** e **Ramser**](http://www.jstor.org/stable/2627477 "The Truck Dispatching Problem"), com o artigo **"The Truck Dispatching Problem"**.

<p></p>

<a href="http://www.jstor.org/stable/2627477" target="_blank" title="Dantzig, George B., and John H. Ramser. 'The truck dispatching problem.' Management science 6.1 (1959): 80-91." class="not-doted">
<img class="polaroid" src="img/the-truck-dispatching.png" alt="Dantzig, George B., and John H. Ramser. 'The truck dispatching problem.' Management science 6.1 (1959): 80-91." width="418" height="161">
</a>

<p></p>

A fundamentação do *Problema de Roteamento de Veículos* está em definir um **conjunto de rotas** a serem percorridas por veículos, reduzindo os custos com transportes até determinados **consumidores**, dado à distância, e obedecendo que: cada rota começa e termina num ponto inicial (**depósito**), todo consumidor é visitado somente uma vez por somente um veículo e a demanda total de qualquer rota não pode ultrapassar capacidade de um veículo.

<img class="polaroid" src="img/vrp.png" alt="Exemplo de Vehicle Routing Problem">

<br>

Existem variações do VRP, baseadas na capacidade do veículo, prioridades de entrega, janela de tempo, etc. Existe um grupo de problemas com o mesmo objetivo do problema de roteamento, dentre eles:

<ul>
    <li class="pointer" title="Edmonds, Jack, and Ellis L. Johnson. 'Matching, Euler tours and the Chinese postman.' Mathematical programming 5.1 (1973): 88-124."><i class="text-orange fa fa-envelope"></i> Problema do carteiro chinês</li>

    <li class="pointer" title="Fleischmann, Bernhard. 'A cutting plane procedure for the travelling salesman problem on road networks.' European Journal of Operational Research 21.3 (1985): 307-317."><i class="text-orange fa fa-briefcase"></i> Problema do caixeiro viajante rodoviário</li>

    <li><i class="text-orange fa fa-suitcase"></i> Problema dos Múltiplos-caixeiros viajantes</li>

    <li><i class="text-orange fa fa-bus"></i> Problema de roteamento com depósito único e multiplos veículos</li>

    <li><i class="text-orange fa fa-motorcycle"></i> Problema de roteamento com múltiplos depósitos e múltiplos veículos</li>

    <li><i class="text-orange fa fa-taxi"></i> Problema de roteamento de veículos capacitados</li>

    <li><i class="text-orange fa fa-clock-o"></i> Problema de roteamento com janelas de tempo</li>
</ul>

<br>

VRPs podem ser classificados de acordo com suas propriedades no que diz respeito aos pedidos a serem cumpridos, a frota disponível, a estrutura de rota, os objetivos e o planejamento considerado. Uma visão geral destas dimensões é dada na seguinte figura, retirada de <a href="http://link.springer.com/article/10.1007/s12159-012-0080-2" target="_blank">`Drexl, Michael. "Rich vehicle routing in theory and practice." Logistics Research 5.1-2 (2012): 47-63`</a>.

<img class="polaroid" src="img/drexl.png" alt="Rich vehicle routing in theory and practice">

<br>

VRP é considerado um problema de otimização combinatorial difícil devido ao tamanho que seu conjunto de localizades pode atingir. 

Por não existir algoritmos exatos que podem confirmar uma busca eficiente no espaço de tempo computacional viável, `Lenstra, Jan Karel, and A. H. G. Rinnooy Kan. "Complexity of vehicle routing and scheduling problems. (1981)"` provam que esse problema é **NP-Difícil** (<small>NP-hard ou NP-complexo</small>).

<a href="https://pt.wikipedia.org/wiki/NP-dif%C3%ADcil" target="_blank" title="NP-difícil" class="not-doted">
<img class="polaroid" src="img/wikipedia-np-hard.png" alt="NP-difícil" width="523" height="163">
</a>

<br>
<br>

<h2 class="text-blue">
    <i class="fa fa-arrow-down bounce-down"></i> Aplicação na Vida Real <i class="fa fa-arrow-down bounce-down"></i>
</h2>

<div class="slide">
<p></p>

#### **Gerenciamento da Cadeia de Suprimentos**

Sistemas logísticos são definidos pelo planejamento, organização e controle de operações de fluxo de mercadorias. Suas atividades principais são: aquisição de matéria-prima, gestão de estoques, processamento de pedidos, compras e armazenagem, manuseio de materiais, programação da produção e entrega ao consumidor final.

Para minimizar custos e tornar todo o processo mais eficiente, são aplicados processos de **Gerenciamento da Cadeia de Suprimentos** (*Supply Chain Management*), integrando, controlando e otimizando o fluxo de bens, produtos, recursos e informações desde os fornecedores até o cliente final.

#### Exemplos práticos

* Transporte de materiais e pessoas

<img src="http://am730.com.br/wp-content/uploads/2012/12/ITINERARIO-DO-ONIBUS-PETROLINA.jpg" alt="" class="polaroid">

* Logística para doações de suprimentos às vítimas de desastres ambientais

<img class="polaroid" src="http://www.charitywater.org/_files/blog/wp-content/uploads/2015/04/blog_post.jpg">

* Roteamento de entrega postal

<img src="http://www.tribunahoje.com/vgmidia/resize/320/324/imagens/58949_ext_arquivo.jpg" class="polaroid">

#### **OpenRouteService**

<a href="http://wiki.openstreetmap.org/wiki/OpenRouteService" target="_blank" title="OpenRouteService">OpenRouteService</a> é um sistema desenvolvido pelo [University of Heidelberg GIScience Research Group](http://giscience.uni-hd.de/) para auxiliar a criação de rotas na plataforma <a href="http://www.openstreetmap.org/" target="_blank" title="OpenStreetMap">OpenStreetMap</a>. Essa plataforma é muito utilizada para criar rotas alternativas em cenários de desastres naturais (Emergency Route Service).

<a href="http://www.openrouteservice.org/" title="OpenRouteService" target="_blank" class="not-doted">
    <img class="polaroid" src="http://wiki.openstreetmap.org/w/images/e/e2/ORS_EmergencyRouteService.png" alt="OpenRouteService">
</a>

<p></p>

#### **Spider Design - SINTEF**

<a href="http://www.sintef.no/" target="_blank">SINTEF</a> é uma instituição de pesquisa sem fins lucrativos, a maior organização da Escandinávia dedicada a atividades de pesquisa e desenvolvimento. <a href="http://www.sintef.no/projectweb/transportation-planning/software/spider/" target="_blank">**Spider**</a> é uma biblioteca para otimização de planejamento de transporte, atuando em alguns cenários de distribuição de pães, jornais, sorvete, sangue.

<img src="img/spider.png" alt="">

</div>

<br>
<br>

<h2 class="text-green">
    <i class="fa fa-arrow-down bounce-down"></i> Referência adicional e Lista de links <i class="fa fa-arrow-down bounce-down"></i>
</h2>

<div class="slide">
<p></p>

<a href="http://www.jstor.org/stable/2627477" target="_blank" title="The truck dispatching problem">
`Dantzig, George B., and John H. Ramser. "The truck dispatching problem." Management science 6.1 (1959): 80-91.`
</a>

<a href="http://onlinelibrary.wiley.com/doi/10.1002/net.3230110211/abstract" target="_blank" title="Complexity of vehicle routing and scheduling problems">
`Lenstra, Jan Karel, and A. H. G. Rinnooy Kan. "Complexity of vehicle routing and scheduling problems." Networks 11.2 (1981): 221-227.`
</a>

<a href="http://dl.acm.org/citation.cfm?id=578533" target="_blank" title="Computers and intractability : a guide to the theory of NP-completeness">
`Garey, Michael R., and David S. Johnson. "Computers and intractability : a guide to the theory of NP-completeness." San Francisco: W.H. Freeman (1979).`
</a>

<a href="http://doi.org/10.1287/moor.10.4.527" target="_blank" title="Bounds and heuristics for capacitated routing problems">
`Haimovich, M. A. R. K., and A. H. G. Rinnooy Kan. "Bounds and heuristics for capacitated routing problems." Mathematics of operations Research 10.4 (1985).`
</a>

<a href="http://doi.org/10.1287/mnsc.40.10.1276" target="_blank" title="A tabu search heuristic for the vehicle routing problem.">
`Gendreau, Michel, Alain Hertz, and Gilbert Laporte. "A tabu search heuristic for the vehicle routing problem." Management science 40.10 (1994): 1276-1290.`
</a>

<a href="http://doi.org/10.1016/0377-2217(92)90192-C" target="_blank" title="The vehicle routing problem: An overview of exact and approximate algorithms">
`Laporte, Gilbert. "The vehicle routing problem: An overview of exact and approximate algorithms." European Journal of Operational Research 59.3 (1992): 345-358.`
</a>

<a href="http://doi.org/10.4236/iim.2012.43010" target="_blank" title="A survey on the vehicle routing problem and its variants">
`Kumar, Suresh Nanda, and Ramasamy Panneerselvam. "A survey on the vehicle routing problem and its variants." (2012).`
</a>

<a href="http://doi.org/10.1023/B:ANOR.0000030690.27939.39" target="_blank" title="Emergency logistics planning in natural disasters.">
`Özdamar, Linet, Ediz Ekinci, and Beste Küçükyazici. "Emergency logistics planning in natural disasters." Annals of operations research 129.1-4 (2004): 217-245.`
</a>

<a href="http://www.dominiopublico.gov.br/pesquisa/DetalheObraForm.do?select_action=&amp;co_obra=185162" target="_blank" title="Um algoritmo híbrido para o problema de roteamento de veículos estático e dinâmico com janela de tempo">
`Alvarenga, Guilherme Bastos. "Um algoritmo híbrido para o problema de roteamento de veículos estático e dinâmico com janela de tempo". Diss. PhD thesis, Universidade Federal de Minas Gerais, 2005.`
</a>
</div>
