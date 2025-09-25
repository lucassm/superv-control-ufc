---
marp: true
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
</style>

# Automação de Subestações

Prof. Lucas Silveira

---

## Evolution of automation systems

Two major developments led to the **advent of distributed control**:

- Integrated circuits.
- Communication systems.

**Supervisory control and data acquisition (SCADA) systems** are widely used for automation of the power sector and represent an **evolving field**.

---

As the **scope of supervisory control applications** changed, so did many of the fundamentals of supervisory control technology.

**During the early years all of the systems were electromechanical**.

The supervisory systems evolved to using:

- solid-state components,
- electronic sensors, and
- analog-to-digital convertors.

---

![bg 70%](./FigurasLeg/eletromec2.png)

---

![bg 60%](./FigurasLeg/utr.jpg)

---

## History of automation systems

In this evolution, the same **remote terminal unit (RTU)** configuration was maintained.

**The companies making the RTUs merely upgraded their technology** without looking at alternate ways of performing the RTU functions.

In the **1980s** process control companies began applying their technology and technical approach to the SCADA electric utility market:

**RTUs used microprocessor-based logic to perform expanded functions**.

---

## Supervisory control and data acquisition (SCADA) systems

> **Definition**: SCADA systems are defined as *a collection* of equipment that will provide an operator at a *remote location* with sufficient information to determine the *status* of particular equipment or a process and cause *actions* to take place regarding that equipment or process, without being physically present.

---

![bg fit](./Figuras2/fig-1.png)

---

![bg fit](./FigurasLeg/automacao-1.png)

---

## SCADA basic functions

The basic SCADA functions include:

- Data acquisition.
- Remote control.
- Human-machine interface.
- Historical data analysis.
- Report writing.

---

# Unidade Terminal Remota

UTR são dispositivos que possuem basicamente:

- UPC: Unidade central de processamento.
- Cartões de E/S digitis e analógicas.
- Canais de comunicação com protocolos diversos.

- Podem ter ou não capacidade de implementação de lógicas programáveis.
- Podem ser distribuídas por bays (vãos) com interligação através de rede.

---

# Unidade Terminal Remota

- Os cartões de E/S digitais podem possuir suporte a SOE permitindo também a sincronização através de IRIG-B.
- Cartões de saída digital muitas vezes dispõem de funcionalidade de *Check Before Operator*.

---

# CLP: Controlador Lógico Progrmável

São dispositivos que também possuem:

- Uma ou mais UCP.
- Cartões de E/S digitais e analógicas.
- Canais de comunicação com diferentes protocolos.
- Sempre são programáveis com linguagens do tipo Ladder ou similar.

> Não é usual aos CLPs terem funções tipo SOE com resolução de milissegundos.
> Podem ser distribuídos por vãos, ligando-se através de uma rede de fibra ótica ou par metálico.

---

# Exemplo de UTR/CLP 

Todas as variáveis de monitoramento e controle são concentradas nas UTR.

A UTR coletava as grandezas analógicas de tensões, correntes e estados digitais da SE, analogicamente e provinha um canal de comunicação para supervisão e controle.

A quantidade de cabos de monitoramentos e controle era grande. A interface com os equipamentos de campo eram basicamente:

- Sinais de corrente e tensão AC
- Sinais de corrente 4 a 20 mA
- Entradas e saídas digitais

---

# Concentrador de Dados

Convertem protocolos da camada de aplicação.

Os concentradores de dados possuem características semelhantes ao módulo CPU das RTU. Eles também são chamados de Gateways de comunicação.

> Sua principal função é coletar informações de outros equipamentos através de canais de comunicação.

---

![bg fit](./Figuras/rtac-sel-1.png)

---

![bg fit](./Figuras/rtac-sel-2.png)

---

![bg fit](./Figuras/rtac-sel-3.png)

---

![bg fit](./Figuras/rtac-sel-4.png)

---

![bg fit](./Figuras/rtac-sel-5.png)

---

# Concentrador de Dados

Com o advento dos **IEDs** os equipamentos de proteção passaram a assumir também tarefas de controle, automação e suoervisão.

A *UTR foi substituída por concentradores de dados ou gateways* de comunicação e toda interface analógica por canais de comunicação e protocolos específicos.

É possível concluir que hoje o alicerce da automação da subestação é a **comunicação** entre dispositivos.

Antes de apresentar os principais protocolo presentes nas subestações é importante conhecer alguns dos principais equipamentos utilizados.

---

# Controlador de Automação Programável

- São equipamentos similares aos CLPs, porém estão destinados a uma automação distribuída.
- Possuem um número limitado de entradas e saídas digitais e analógicas pois são instalados próximos ao equipamento alvo da automação.
- Podem conter entradas RTD e interfaces analógicas para TCs e TPs.

---

# Medidores de Faturamento

São equipamentos utilizados para medição precisa de grandezas analógicas como:

- Correntes e tensões
- Potências
- Energias
- Fator de Potência
- Frequência

> São ligados a **TCs de medição**.

---

# Medidores de Qualidade de Energia

São equipamentos utilizados para medição precisa de grandezas analógicas como:

- Correntes e tensões
- Harmônicas
- Taxa de distorções harmômica
- Sag/Swell
- Curva de carga

Ligados a TCs de proteção.

---

# Relés de Proteção Digital

- São dispositivos de proteção dedicados ou multifunção.
- Além da função primária de proteção pode também acumular funções de:
  - Controlador de Bay
  - Automatizador de processos
  - Medidor de variáveis analógicas

Relés de proteção devem sempre prover meios de sincronismo de seus relógios internos para geração de oscilografias e sequenciais de eventos precisos.

Alguns relés também são capazes de realizar medições de sincro-fasores.

---

![bg fit](./Figuras/ied-sel-1.png)

---

![bg fit](./Figuras/ied-sel-2.png)

<!-- ---

# Relés de Proteção Digital: Lógicas

- Utilização de lógica booleana e aritmética básica, além de temporizadores, biestáveis, contadores, variáveis auxiliares, etc.
- Disposnibilidade de utilizar nas equações variáveis internas de proteção, controle, I/O físicas, comunicação, etc.
- Facilidade de criação de novas funções e automatismos. 

---

# Relés de Proteção Digital: IHM

- O uso de relés de proteção digitais permite que através de seu painel frontal sejam programadas várias funções de controle pela interface com o usuário, por exemplo:

- Mensagens de texto
- LEDs de sinalização
- Botões programáveis
- Mímico para controle local do Bay

--- -->

---

## Intelligent Electronic Devices (IEDs)

The industry standard definition of an IED is:

**Any device incorporating one or more processors with the capability to receive or send data/control from or to an external source (e.g., electronic multifunction meters, digital relays, and controllers).**

IEDs have been deployed extensively in power automation systems recently, and the shift from RTUs to IEDs is evident due to the integration and interoperability features of the IEDs.

---

## Evolution of IEDs

IEDs were **introduced in the early 1980s** with microprocessor-based control features.

The deployment of IEDs is revolutionizing the protection, substation and distribution automation.

The protection relay migrated **from single-function conventional electromechanical** types **to multi-function microprocessor-based relays**.

Considerable **savings were achieved in relay panel and switchgear costs** by the adoption of the multi-function microprocessor-based relays.

---

![bg 80%](./FigurasLeg/eletromec.png)

---

## Evolution of IEDs

IED revolution started when **other functionalities** like accurate voltage and current phasor measurement, waveform capture, and metering were being incorporated into the relays.

The growth in:

- Communication infrastructure,
- Standardization of protocols, and
- Interoperability

Were major factors that led to the IED explosion. **IEDs are now the eyes, ears, and hands of the automation systems in a power utility**.

---

## Evolution of IEDs

These savings can be summarized in the following categories:

1. Lower installation and panel assembly cost
2. Shorter commissioning and maintenance times
3. Shorter system recovery time after a disturbance
4. Less revenue loss due to wrong settings and IED malfunction
5. Higher system reliability due to automation, integration, and adaptive settings
6. Smaller control houses

---

## IED functional block diagram

The modern IED architecture ensures that the device is:

- multipurpose,
- modular in nature,
- flexible and adaptable, and
- has robust communication capabilities.

Communication capabilities include multiple selectable protocols, multi-drop facilities with multiple ports, and rapid response for real-time data.

---

## IED functional block diagram

IEDs also have tremendous data-processing capability for a variety of functions, for various applications like protection and metering.

IEDs have event recording capability that can be very useful for post-event analysis, for fault waveform recording, and for power quality measurements.

IEDs can also accept and send out analog and digital signals with selectable ratings, thus making the IEDs versatile.

---

![bg fit](./Figuras2/fig-8.png)

---

## 2.5.3 Hardware and software architecture of the IED

The hardware of IED should be designed with the future adaptability requirement in mind, whereas the software structure should ensure the independent:

- protection,
- control,
- metering, and
- communication functions.

> IED hardware design utilizes draw out–type cards which is a great advantage, as the replacement can be done easily without disconnecting the terminal wires and removing the IED from the panel.

---

![bg fit](./Figuras2/fig-10.png)

---

## 2.5.3 Hardware and software architecture of the IED

IED has the capability of **waveform capture and disturbance analysis capability**.

Metering and demand values recording are other features.

IED has the capability of programmable logics that eliminates an additional PLC usage.

---

![bg fit](./Figuras2/sel-751-manual/fig-1.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-2.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-3.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-4.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-6.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-8.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-9.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-10.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-11.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-12.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-13.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-14.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-15.png)

---

![bg fit](./Figuras2/sel-751-manual/fig-16.png)

---

## IED communication subsystem

The IED should support:

- Different protocols for multi-port communication and different media
- Should have flexible and open communication architecture,
- HMI interface,
- Remote access port, and
- Direct communication to other IEDs for protection purposes.

---

## 2.5.3 Hardware and software architecture of the IED

The IEDs have plug-and-play communication modules that can support a variety of protocols.

The advantage of these modules is that they can be replaced in the field in case of a change in communication requirement.

The IEDs use the communication port and optical port for fiber optical communication or electrical port (RS-232 or RS-485) and will also have service port for remote access via a modem.

---

## Merging units and IEDs

![bg fit left:60%](./Figuras2/fig-14.png)
