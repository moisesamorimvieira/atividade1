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

1. LEDs via GPIO: Controla LEDs nos pinos 11, 12 e 13.

2. Temporizador Periódico: Usa add_repeating_timer_ms() para alternar LEDs a cada 3000 ms.

3. Callback: semaforo_callback() desliga todos os LEDs e liga o LED correspondente ao estado atual do semáforo.

4. Comunicação Serial: Inicializa com stdio_init_all() para exibir mensagens no terminal.

5. Controlo de Fluxo: Loop contínuo while(true) e sleep_ms() para pausar.

6. Estado do Semáforo: Variável estado_semaforo rastreia o estado atual do semáforo.

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
 
