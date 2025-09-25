---
marp: true
paginate: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Akaya+Kanadaka&family=Andika:ital,wght@0,400;0,700;1,400;1,700&family=Josefin+Slab:ital,wght@0,100..700;1,100..700&family=League+Spartan:wght@100..900&family=Spectral:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
</style>

<style>
    section {
        font-family: "Andika", serif;
        font-weight: 400;
        font-style: normal;
        font-size: 32px;
    }
    strong {
        color: rgb(196, 89, 89)
    }
    h2 {
        color: rgb(48, 103, 167)
    }
    em {
        color: rgb(196, 89, 89)
    }

    .columns {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 1rem;
    }
</style>

# Supervisão e Controle de Sistemas Elétricos de Potência

## A Subestação e seus equipamentos

Prof. Lucas Silveira

---

# A subestação

O objeto da automação de sistemas elétricos é a **subestação** (SE).

> **Definição**: Uma SE é um componente do sistema elétrico responsável pelo *controle* e *manobra* de um sistema de transmissão elétrica, adequando os níveis de tensão e funcionamento como pontos de entrega para consumidores de grande porte ou redes de distribuição de energia elétrica.

---

As subestações (SE) são compostas por conjuntos de elementos, com
funções específicas no sistema elétrico, denominados **vãos (bays)** que permitem a composição da subestação em módulos.

As SE distribuidoras, usualmente, são compostas pelos seguintes
vãos:

- entrada de linha (EL).
- saída de linha (SL).
- barramentos de alta e média tensão (B2 e B1).
- vão de transformação (TR).
- banco de capacitor ou vão de regulação (BC).
- saída de alimentador (AL).

---

Cada vão da subestação deve possuir dispositivos de proteção (relés) e equipamento de disjunção com a finalidade de limitar os impactos proporcionados por ocorrências no sistema elétrico tais como:

- descargas atmosféricas.
- colisão.
- falhas de equipamentos.
- curtos-circuitos, etc.

---

Como regra geral, as funções em uma subestação são:

- Monitoração de "status" de equipamentos.
- Medição.
- Proteção de linha, transformadores, barra, reator, perda de sincronismo etc.
- Supervisão das proteções.
- Religamento automático.
- Localização de falha na linha.
- Telecomandos.
- Proteção de falha de disjuntor.

---

- Intertravamentos.
- Monitoração de sobrecarga em transformadores.
- Controle de tensão.
- Fluxo de reativos.
- Corte seletivo de cargas.
- Sincronização.
- Alarmes em geral.
- Registro de seqüência de eventos.

---

- Oscilografia.
- Interface humana.
- Impressão de relatórios.
- Interface com os Centros de Operação de Sistema.
- Autodiagnose.

---

# Equipamentos primários existentes em uma SE

Os mais comuns são:

- Disjuntores
- Chaves Seccionadoras
- Transformadores
- Sistemas auxiliares de alimentação
- Bancos de capacitores
- Reatores
- Geradores

---

![bg 70%](./Fotos-SE-UFC/se_pici.jpg)

---

![bg 70%](./Fotos-SE-UFC/se_pici_2.jpg)

---

![bg 40%](./Fotos-SE-UFC/se_pici_138.jpg)

---

# Códigos Operacionais dos equipamentos

Em uma subestação cada equipamento é **identificado** por um **código** que identifica:

- Tipo de equipamento.
- Faixa de tensão.
- Posição dentro da subestação.

A nomenclatura mais usual utilizada nos **diagramas unifilares**, em geral é constituída de quatro dígitos **XYZW**.

---

O primeiro dígito X indica o tipo de equipamento como descrito na Tabela abaixo.

| Código | Equipamento                                        |
| :----: | :------------------------------------------------- |
|   0    | Equipamento não interruptor (trafo, reator, linha) |
|   1    | Disjuntor                                          |
|   2    | Religador                                          |
|   3    | Chave seccionadora                                 |
|   4    | Chave fusível                                      |
|   5    | Chave a óleo                                       |

---

| Código | Equipamento                     |
| :----: | :------------------------------ |
|   7    | Pára-raio                       |
|   8    | Transformador de potencial (TP) |
|   9    | Transformador de corrente (TC)  |

---

O Segundo dígito Y, define a tensão de operação do equipamento, sendo que no caso de transformadores será considerada a maior tensão de operação.

| Código |     Faixa de Tensão      |   Cor    |
| :----: | :----------------------: | :------: |
|   1    |  1kV a 25 kV (13,8 kV)   | Laranja  |
|   2    |  51 kV a 75 kV (69 kV)   |  Verde   |
|   3    | 76 kV a 150 kV (138 kV)  |  Preto   |
|   4    | 151 kV a 250 kV (230 kV) |   Azul   |
|   5    | 251 kV a 550 kV (500 kV) | Vermelho |

---

O terceiro dígito Z, indica o tipo de equipamento, enquanto o quarto dígito W indica a seqüência ou posição do equipamento.

As letras (C, F, I, J, L, M, N, P, S, V e Y) são utilizadas para nomear linhas de transmissão ou de distribuição, guardando, quando possível associação ao nome da instalação.

---

| Código | Equipamento                       |  Sequência  |
| :----: | :-------------------------------- | :---------: |
|   A    | Transformador de aterramento      |   A1 a A9   |
|   B    | Barramento                        |   B1 a B9   |
|   D    | Equipamento de transferência      |   D1 a D9   |
|   E    | Reator                            |   E1 a E9   |
|   G    | Gerador                           |   G1 a G9   |
|   K    | Compensador Síncrono              |   K1 a K9   |
|   H    | Banco de Capacitor                |   H1 a H9   |
|   PO   | Pára-raios                        | PO-1 a PO-9 |

---

| Código | Equipamento                       |  Sequência  |
| :----: | :-------------------------------- | :---------: |
|   R    | Regulador de tensão               |   R1 a R9   |
|   T    | Transformador de força            |   T1 a T5   |
|   T    | Transformador de serviço auxiliar |   T6 a T9   |
|   X    | Conjunto de medição               |   X1 a X9   |
|   U    | Transformador de potencial        |   U1 a U9   |
|   Z    | Transformador de corrente         |   Z1 a Z9   |
|   W    | Resistor de aterramento           |   W1 a W9   |

---

![bg fit](./Figuras/unifilar-se-ufc-geral.png)

---

![bg fit](./Figuras/unifilar-se-ufc-1.png)

---

![bg fit](./Figuras/unifilar-se-ufc-2.png)

---

![bg fit](./Figuras/unifilar-se-ufc-3.png)

---

![bg fit](./Figuras/unifilar-se-ufc-4.png)

---

![bg 60%](./Figuras/rede_pici_comunicacao.png)

---

![bg 60%](./Figuras/bays/image48.jpeg)

---

![bg 60%](./Figuras/bays/image49.jpeg)

---

![bg 60%](./Figuras/bays/image55.jpeg)

---

# Contatos Digitais

- Os equipamentos de campo de uma SE normalmente provêm saídas e entradas digitais para informar sua condição ou alarmes e receber comandos.
- As entradas digitais utilizam opto-acopladores para prover isolamento elétrico.
- As saídas podem ser a relé ou utilizando eletrônica de potência.

---

# Contatos Digitais

Os **optoacopladores** de uma entrada digital possui um LED na interface com exterior. Esse LED quando excitado envia luz para um foto-transistor que envia o sinal elétrico para o dispositivo. 

É importante verificar o nível de tensão. Normalmente estas entradas digitais utilizam 125 Vcc.

Para as saídas digitais é comum a utilização de relés. Estes possuem uma carga máxima relativa aos contatos metálicos. Esses relés podem possuir contatos NF e NA.

---

# Transdutores de Sinais

Fornecem sinais analógicos de grandezas a serem supervisionadas como:

- Humidade.
- Temperatura.
- Pressão.
- Nível de óleo.

Geralmente fornecem sinais analógicos na faixa de: **4 a 20 mA** ou 10 a 10V.

> Os sinais de 4 a 20 mA são mais utilizados pois podem alcançar distâncias maiores e são mais imunes à ruído.

---

# Disjuntores

> **Definição**: São equipamentos utilizados para proteção dos circuitos elétricos da SE. Estes possuem capacidade para interrupção de correntes elétricas da ordem de kA.

- Disjuntores a óleo: pequeno volume, grande volume;
- Disjuntores a gás (SF6);
- Disjuntores a vácuo (geralemnte só utilizados em subestações industriais).

---

No caso de abertuda dos contatos de um equipamento interruptivo, uma **tensão elevada surgirá nos seus terminais** e o ar ao redor se ionizará, provocando um arco elétrico.

Dessa forma, os disjuntores devem ter seus **contatos imersos em substância inerte**.

O mecanismo de abertura deste dispositivo deve ser extremamente rápido. Para tal existe uma **mola** que é comprimida no fechamento e liberada durante a abertura, completando sua abertura em tempos inferiores a *100ms*.

---

![bg 40%](./Fotos-SE-UFC/disjuntor_69.jpg)

---

![bg fit](./Figuras/disjuntor-e-chave.png)

---

# Interface com Disjuntores

<div class="columns">

<div>

- Contatos:
  - 52A (NA): Fechado e 52B (NF): Aberto.
  - Mola descarregada.
  - Falta de alimentação CC.
  - Baixo nível de SF6.
  - Chave L/R.
  - Posição inserido, extraído e teste.

</div>

<div>

- Entradas (comandos):
  - Abrir e Fechar

Além da interface digital básica, podem estar disponíveis as correntes das fases via TCs internos e o nível de SF6 em 4-20mA.

</div>

</div>

---

![bg fit](./Figuras/contatos-auxiliares-disjuntor.png)

---

# Chaves Seccionadoras

As chaves seccionadoras (CS) são dispositivos de manobra e possuem seus contatos expostos. Com isso não podem interromper circuitos energizados.

As CS são normalmente associadas a disjuntores nas seções da SE.

O mecanismo de operação neste caso não necessita de alto desempenho. A abertura e fechamento ocorre geralmente em alguns segundos.

---

![bg 40%](./Fotos-SE-UFC/seccionador_lamina.jpg)

---

![bg 50%](./Figuras/esquematico-chave-sec.png)

---

# Interface com chaves seccionadoras

<div class="columns">
<div>

- Contatos:
  - 89A (NA): Fechado e 89B (NB): Aberto.
  - Transição (89A e 89B abertos).
  - Defeito (89A e 89B fechados).
  - Falta de alimentação CA e CC.
  - Chave L/R.

</div>

<div>

- Entradas (comandos)
  - Abrir e Fechar.
- Sinais analógicos:
  - Posição angular (4-20 mA)
  - Torque motor (4-20 mA)

</div>
</div>

---

# Transformadores

Os transformadores são o principal e mais caro equipamento de uma SE.

Sua funcionalidade é: *adequar os níveis de tensão, normalmente das linhas de transmissão e sub-transmissão aos níveis de tensão da distribuição*.

Além das **tensões de entrada e saída**, são especificados segundo a **potência** exigida pelos circuitos alimentadores da SE.

---

# Transformadores

Podem possuir regulação da tensão de saída dentro do próprio transformador ou através de equipamentos externos chamados de **LTC (Load Tap Changer)**.

Os níveis de entrada presentes no Brasil são 750, 500, 345, 230, 138 e 69kV. A saída depende dos circuitos alimentadores. Para redes de distribuições urbanas normalmente utiliza-se 13.8kV.

---

# Transformadores

Os transformadores podem ser trifásicos ou monofásicos. Normalmente possuem um enrolamento primário e um secundário, mas podem possuir mais enrolamentos.

Dependendo dos aspectos técnico-econômicos pode ser aplicado um banco de transformadores monofásicos ao invés de um único transformador trifásico.

---

![bg 40%](./Fotos-SE-UFC/trafo_69.jpg)

---

![bg 40%](./Fotos-SE-UFC/trafo_69_2.jpg)

---

![bg fit](./Figuras/quadro-trafo.png)

---

# Interface com Transformadores

<div class="columns">

<div>

- Contatos:
  - Alarmes de temperatura do óleo e enrolamentos.
  - Atuação do relé Buchholz.
  - Estágios de ventilação forçada.
  - Falha no circuito de ventilação forçada.
  - Proteção intrinseca atuada.

</div>

<div>

- Contatos:
  - Posição do tape.
  - Válvula de alívio de pressão atuada.
  - Nível mínimo e máximo de óleo atuado.
  - Monitor de ruptura de membrana atuado.

</div>

</div>

---

# Interface com Transformadores

- Comandos:
  - Liga/Desliga ventilação forçada.
  - Sobe/Desce tape.
- Sinais analógicos:
  - Correntes das fases (TCs internos).
  - Temperatura do óleo, enrolamento e ambiente (RTDs).
  - Gases e agua dissolvidos no óleo (4 - 20 mA ou comunicação).

---

# Sistema auxiliar de alimentação

Toda a alimentação dos equipamentos da subestação é fornecida pelo **serviço auxiliar**. Este é alimentado por transformadores derivados do(s) transformador(es) principal(is).

Em um caso de falha na linha de transmissão de entrada da SE, todos os equipamentos devem ser manter ativos.

Isso é possível devido a **banco de baterias** e em alguns casos **geradores de emergência**.

---

![bg left: 80%](./Figuras/banco-baterias.jpeg)
![bg 80%](./Figuras/quadros-ca-cc.jpeg)

---

# Sistema auxiliar de alimentação

A maioria dos equipamentos e dispositivos utilizados na SE são alimentados por **corrente contínua de 125Vcc**.

Este sistema normalmente é abrigado na **casa de controle** da SE.

---

# Interface com sistema auxiliar

- Contatos:
  - Falha no retificador.
  - Falha de alimentação CA.
  - Alarme de nível baixo ou alto da tensão da bateria.
  - Partida do gerador de emergência.
- Sinais analógicos:
  - Corrente e tensão CC (4-20 ma ou comunicação).
  - Corrente e tensão CA (TCs e TPs).

---

# Banco de Capacitores

Um banco de capacitores é o conjunto formado por associação série/paralelo de capacitores individuais. A função desse equipamento é corrigir o fator de potência da energia entregue pela SE.

Os bancos podem ser associados e automatizados para controle do reativo através de disjuntores e seccionadoras.

---

# Reatores

Os reatores em derivação são empregados para controlar as tensões nos barramentos, em regime permanente, compensando a capacitância das linhas de transmissão no período de carga leve, e para a redução das sobrecorrentes, nos surtos de manobra.

Assim como o banco de capacitores, o reator também pode ser automatizado.

---

# Casa de controle

> A casa de controle de uma SE abriga os equipamentos mais sensíveis de uma SE.

Normalmente computadores, retificadores, painéis de controle e relés.

Para o cabeamento de supervisão e controle, os **relés** e controladores podem ser instalados fora da casa e próximos aos equipamentos de campo.

No caso de **relés instalados no campo**  deve-se garantir a proteção destes dispositivos eletrônicos contra altas diferenças de temperaturas, radiação eletromagnética e outras adversidades deste ambiente.

---

# Casa de controle

A casa de controle pode ser de alvenaria ou pré-fabricada.

> Uma SE pode ser **assistida** ou **não assistida**.

No caso da **assistida**, ela deve possuir infraestrutura para suportar os técnicos que se revezarão em turnos para operar.

No caso de **desassistida**, pelo menos um banheiro é exigido pela NR-10.

---

![bg 40%](./Fotos-SE-UFC/casinha.jpg)

---

# Como medir e controlar tensões de até 750 kV e correntes acima de 1kA?

É necessário converter os sinais elétricos presentes na SE, para isso utiliza-se:

- Transfomadores de Potencial - TPs
- Transformadores de Corrente - TCs
- IEDs
- Transdutores

---

# Transfomadores de Potencial - TPs

- Utiliza o mesmo princípio dos transformadores de potência, transformando potenciais elevados em níveis reduzidos de tensão para sistemas de proteção e automação.
- Os valores de tensão secundária são em geral, de 115V ou 69V dependendo do tipo de ligação em estrela ou delta.

As tensões de saída do TP podem sofrer sobrecargas de até 110% sem distorção do sinal.

Os TPs devem estar classificados quanto a sua precisão nas classes de 0,3 / 0,6 / 1,2 para medição e 2,5 / 5,0 / 10 para proteção.

Os TPs podem ser indutivos, capacitivos ou resistivos.

---

![bg 40%](./Fotos-SE-UFC/tp_69.jpg)

---

# Transformadores de Corrente

- Tranforma níveis de correntes elevados em níveis reduzidos para sistemas de proteção e automação.
- Os valores de corrente secundária são em geral, de 1A ou 5A, dependendo do tipo de TC.

No caso dos TCs as sobrecargas podem ocasionar danos físicos devido aos esforços dinâmicos. Por esse motivo, os TCs possuem um faotr de serviço que garante a sobre carga mometânea sem saturação do TC e danos físicos ao mesmo.

---

![bg 40%](./Fotos-SE-UFC/tc_69.jpg)

---

# Transformadores de Corrente

As principais partes de um transformador de corrente são:

- Núcleo de ferro.
- Enrolamento secundário.
- Condutor primário.

Alguns TCs não têm um condutor primário. Nesses casos o primário é a própria linha ou barramento.

> Algumas vezes o núcleo e seu enrolamento secundário são instalados diretamente na bucha dos disjuntores ou transformadores. São os **TCs de bucha**.

---

# Transformadores de Corrente

Alguns transformadores de corrente podem ter um primário que consiste de algumas espiras.

> Normalmente, o número de espiras primárias é igual a 1.

A carga conectada ao terminal do TC é chamada de **burden**.

Geralmente para um único TC é possível encontrar **vários tapes no enrolamento**, atendendo assim à diversas relações de transformação.

---

# Transformadores de Corrente

Existem TCs para proteção e para medição. Os TCs de proteção devem suportar correntes de até 20 vezes a corrente nominal, equanto os TCs de medição devem possuir maior exatidão na faixa nomimal.

Exibir os dados de placa de um transformador de potência.

---

# Transformadores de Corrente

A saturação é causada pelo núcleo de ferro utilizado na fabricação dos TCs que não é linear em toda a sua faixa.

A saturação causa a degradação do sinal de corrente secundária prejudicando o sistema de proteção e automação.

---

# Arranjos de Subestações

- Barra simples.
- Dupla barra simples.
- Barra simples seccionada.
- Barra principal e de transferência.
- Barra dupla, um disjuntor.
- Barra dupla, duplo disjuntor.
- Barra dupla com disjuntor e meio.
- Barramento em anel.

---

![bg fit](./Figuras/barra-simples.png)

---

# Arranjo Barra Simples

<div class="columns">

<div>

## Vantagens

- Instalação simples.
- Baixo custo.
- Operação simplificada.

</div>

<div>

## Desvantagens

- Falha na barra ou disjuntor de entrada desliga toda a SE.
- Manutenção nos alimentadores interrompe o fornecimento.
- Ampliação da SE requer o desligamento da mesma.

</div>

</div>

---

![bg fit](./Figuras/dupla-barra-simples.png)

---

# Arranjo Dupla Barra Simples

<div class="columns">

<div>

## Vantagens

- Cada circuito tem dois disjuntores dedicados.
- Flexibilidade de transferência de circuitos entre as barras.
- Qualquer disjuntor de entrada pode ser retirado para manutenção sem prejuízo ao fornecimento.

</div>

<div>

## Desvantagens

- Custo mais elevado.
- Perda da metade das cargas se o disjuntor de interligação não estiver ligado.

</div>

</div>

---

![bg fit](./Figuras/barra-simples-seccionada.png)

---

# Arranjo Barra simples seccionada

<div class="columns">


<div>

## Vantagens

- Maior continuidade no fornecimento.
- Facilidade de manutenção.
- É indicado para funcionar com duas ou mais fontes de energia.
- Em caso de falha da barra, somente são desligados os consumidores ligados à seção.

</div>

<div>

## Desvantagens

- Não se pode transferir uma linha de uma barra para outra.
- A manutenção de um disjuntor deixa fora de serviço a linha correspondente.
- Esquema de proteção é mais complexo.

</div>

</div>

---

![bg fit](./Figuras/barra-principal-e-transferencia.png)

---

# Arranjo Barra principal e de transferência

<div class="columns">

<div>

## Vantagens

- Custo relativamente baixos.
- Possibilidade de ampliação da SE sem desenergização.
- Qualquer disjuntor pode ser retirado de serviço para manutenção.
- Fácil ampliação.
</div>

<div>

## Desvantagens

- Requer disjuntor extra para a conexão entre as barras.
- Falha no barramento em um dos disjuntores resulta no desligamento da SE.
- Esquema de proteção é mais complexo.
</div>

</div>

---

# Arranjo Barra dupla, um disjuntor

<div class="columns">

<div>

## Vantagens

- Permite alguma flaxibilidade com ambas as barras em operação.
- Qualquer uma das barras pode  ser isolada para manutenção.
- Facilidade de transferência dos circuitos entre as barras.

</div>

<div>

## Desvantagens

- Requer um disjuntor extra para conexão entre as barras.
- São necessárias quatro chaves seccionadoras por circuito.
- A proteção do barramento pode causar a perda da SE.
- Alta exposição a falhas no barramento.

</div>

</div>

---

# Barra dupla disjuntor duplo

<div class="columns">

<div>

## Vantagens

- Muito mais flexível.
- Maior confiabilidade.

</div>

<div>

## Desvantagens

- Arranjo mais complexo.
- Custo elevado.

</div>

</div>

---

# Barra Dupla com disjuntor e Meio

<div class="columns">

<div>

## Vantagens

- Maior flexibilidade de manobra e rápida recomposição.
- Falha nos disjuntores adjacentes às barras retiram apenas um circuito de serviço.
- Manobras simples.
- Qualquer das barras pode ser retirada para manutenção.

</div>

<div>

## Desvantagens

- Operação complicada.
- Meio disjuntor adicional por circuito.

</div>

</div>

---

# Barramento em Anel

<div class="columns">

<div>

## Vantagens

- Baixo custo.
- Flexibilidade para manutenção nos disjuntores.
- Qualquer disjuntor pode ser retirado para manutenção sem interrupção de fornecimento.

</div>

<div>

## Desvantagens

- Se uma falta ocorre durante a manutenção, o anel pode ser separado em duas seções.
- Esquema de proteção mais complexo.

</div>

</div>

---

# Obrigado!

## Prof. Lucas Silveira

lucassmelo@dee.ufc.br
