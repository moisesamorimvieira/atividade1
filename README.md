<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=02A6F4&height=120&section=header"/>
<h1 align="center">Embarcatec | Clock e Temporizadores /  Atividade 1: Temporizador periódico. </h1>

<div align="center">  
  <img width=40% src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=02A6F4&style=for-the-badge"/>
</div>

## Objetivo do Projeto

Com o emprego da função add_repeating_timer_ms(), presente na ferramenta Pico SDK, projete um semáforo com temporização de 3 segundos para cada alteração de sinal. O fluxograma simplificado de atuação do semáforo pode ser visualizado na Figura 1. Nesta prática, será necessário simular os seguintes componentes (configuração sugerida está presente na Figura 2)

1) Microcontrolador Raspberry Pi Pico W.
2) 03 LEDs (vermelho, amarelo e verde).
3) 03 Resistores de 330 Ω.

## 🗒️ Lista de requisitos

1) O acionamento dos LEDs (sinais do semáforo) deve iniciar na cor vermelha, conforme orientação presente na Figura 1, alterando para amarela e, em seguida, verde.
2) O temporizador deve ser ajustado para um atraso de 3 segundos (3.000ms).
3) A mudança de estado dos LEDs deve ser implementa na função de call-back do temporizador, a exemplo da rotina trabalhada na aula síncrona - repeating_timer_callback().
4) A rotina principal, presente no interior da estrutura de repetição while, deve imprimir algum tipo de informação a cada segundo (1.000 ms) - a mensagem enviada pela porta serial fica a critério do discente.
5) Com o emprego da Ferramenta Educacional BitDogLab, faça um experimento com o código deste exercício utilizando o LED RGB – GPIOs 11, 12 e 13.

## 🛠 Tecnologias

1. **Git e Github**;
2. **VScode**;
3. **Linguagem C**;
4. **Software de emulação PuTTy. (Opcional para testes)**
5. **Extensões no VScode do Raspberry Pi Pico Project e CMake**
6. **Wokwi**;

## 🔧 Funcionalidades Implementadas:

• Controlo de LEDs via GPIO: O código inicializa e configura três pinos GPIO (11, 12 e 13) como saídas para controlar os LEDs vermelho, amarelo e verde, respetivamente [o código]. A função gpio_put() é utilizada para ligar ou desligar os LEDs [o código]. O RP2040 pode conectar um dos seus periféricos internos a cada GPIO.
•
Temporizador Periódico: A função add_repeating_timer_ms() configura um temporizador que chama a função semaforo_callback() a cada 3000 milissegundos, permitindo a transição automática entre os estados do semáforo. A biblioteca pico/time.h oferece funções para criar timestamps, colocar o microcontrolador em sleep e usar alarms e temporizadores repetitivos.

• Função de Callback: A função semaforo_callback() é um callback, ou seja, é executada automaticamente quando o temporizador dispara [o código]. Essa função é responsável por desligar todos os LEDs e ligar o LED correspondente ao estado atual do semáforo, permitindo a mudança sequencial das luzes [o código]. A função alarm_pool_add_repeating_timer_us adiciona um temporizador repetitivo ao alarm pool.

• Comunicação Serial: A função stdio_init_all() inicializa a comunicação serial, permitindo que o programa exiba mensagens através do terminal, como o tempo decorrido em milissegundos. A biblioteca pico_stdio oferece suporte para entrada e saída através de UART, USB ou semi-hosting.

• Controlo de Fluxo: O programa utiliza um loop while(true) para executar continuamente e imprimir o tempo decorrido a cada segundo. O código também utiliza a função sleep_ms() para pausar a execução por um segundo.

• Controlo de Estado do Semáforo: O código utiliza uma variável inteira estado_semaforo para rastrear o estado atual do semáforo (0 = vermelho, 1 = amarelo, 2 = verde). Este estado é usado para determinar qual LED deve ser ligado no callback do temporizador. Além disso, o código demonstra o uso de algumas funcionalidades importantes do SDK, como:

• A inclusão de headers para acesso às funcionalidades da biblioteca como stdio.h para a função printf, pico/stdlib.h para a inicialização padrão, hardware/gpio.h para controlar os GPIOs e pico/time.h para usar funções de tempo.

• Uso de funções do SDK para inicialização, manipulação de GPIO, temporização, e saída para stdout. Em resumo, o código implementa um semáforo básico que utiliza os recursos de tempo e GPIO do RP2040, incluindo a capacidade de exibir mensagens na porta serial. Os GPIOs são usados para controlar LEDs, e um temporizador periódico com uma função de callback é usado para alternar as luzes do semáforo.

## 💻 Desenvolvedores
 
<table>
  <tr>
    
<td align="center"><img style="" src="https://avatars.githubusercontent.com/u/96251377?v=4" width="100px;" alt=""/><br /><sub><b> Moises Amorim </b></sub></a><br />👨‍💻</a></td>

  </tr>
</table>


## 🎥 Demonstração: 

<div align="center">
  <figure>  
    
    
<figcaption>

**Figura 1** - Demo do Projeto no Wokwi.com - Acessível em: https://wokwi.com/projects/421539184641481729
    </figcaption>
  </figure>
</div>
 
