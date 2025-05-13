# Projeto-10
# Resumo do Projeto de Timer

## O que foi feito neste projeto

- Criação de um timer estilo Pomodoro, com funcionalidades de iniciar, pausar, parar e ajustar o tempo.
- Manipulação do DOM para mostrar e esconder botões conforme o estado do timer.
- Implementação de lógica para contagem regressiva de minutos e segundos.
- Utilização de módulos JavaScript para organizar o código em arquivos separados (`controls.js`, `timer.js`, `index.js`).
- Uso de funções para controlar o estado dos botões e do timer.
- Adição de controles para ligar/desligar o som (apenas visual, sem áudio real).
- Prática de eventos do JavaScript (`addEventListener`) para interatividade dos botões.
- Aprendizado sobre atualização dinâmica de elementos HTML usando JavaScript.
- Utilização de `setTimeout` para criar a contagem regressiva.
- Prática de boas práticas de organização de código e reutilização de funções.

## Principais funcionalidades

- **Iniciar Timer:** Começa a contagem regressiva do tempo definido.
- **Pausar Timer:** Interrompe temporariamente a contagem do timer.
- **Parar Timer:** Reseta o timer para o valor inicial.
- **Ajustar Tempo:** Permite definir um novo tempo para o timer.
- **Alternar Som:** Mostra visualmente se o som está ligado ou desligado (apenas interface).

## Passo a passo para refazer as funcionalidades

1. **Estrutura HTML**
   - Crie botões para play, pause, stop, set, sound-on e sound-off.
   - Adicione elementos para exibir minutos e segundos.

2. **Organização do JavaScript**
   - Separe o código em módulos: `controls.js` (controle dos botões), `timer.js` (lógica do timer) e `index.js` (integração e eventos).

3. **Controle dos Botões (`controls.js`)**
   - Implemente funções para mostrar/esconder botões conforme o estado do timer.
   - Crie uma função para solicitar ao usuário o novo tempo via `prompt`.

4. **Lógica do Timer (`timer.js`)**
   - Implemente a função de contagem regressiva usando `setTimeout`.
   - Atualize o display de minutos e segundos dinamicamente.
   - Adicione funções para resetar, pausar e atualizar o tempo do timer.

5. **Integração e Eventos (`index.js`)**
   - Associe eventos de clique aos botões para chamar as funções corretas dos módulos.
   - Garanta que o timer e os controles estejam sincronizados.

6. **Detalhes Extras**
   - Use manipulação de classes CSS para mostrar/esconder botões.
   - Certifique-se de limpar o timer com `clearTimeout` ao pausar ou resetar.

## Pontos de aprendizado

- Como manipular classes CSS via JavaScript para mostrar/esconder elementos.
- Como criar e importar módulos ES6.
- Como atualizar o conteúdo de elementos HTML dinamicamente.
- Como solicitar entrada do usuário com `prompt` e tratar valores retornados.
- Como controlar o fluxo do timer (iniciar, pausar, resetar).
- Como limpar timers com `clearTimeout`.

---

## O que foi implementado nos arquivos JavaScript

### `elements.js`
- Seleção dos elementos do DOM (botões e displays de minutos/segundos) usando `document.querySelector`.
- Exportação desses elementos para serem usados nos outros módulos.

### `controls.js`
- Funções para controlar a exibição dos botões conforme o estado do timer (`play`, `pause`, `reset`).
- Função `getMinutes` que usa `prompt` para solicitar ao usuário um novo valor de minutos.
- Exportação das funções principais para uso no arquivo principal.

### `timer.js`
- Função principal que recebe os elementos do display e função de reset dos controles.
- Implementação da lógica de contagem regressiva usando `setTimeout`.
- Função `updateDisplay` para atualizar dinamicamente os minutos e segundos no display.
- Função `reset` para zerar o timer e limpar o timeout.
- Função `countdown` que faz a contagem regressiva, verifica se terminou e executa ações finais (reset, som).
- Função `updateMinutes` para atualizar o valor de minutos.
- Função `hold` para pausar o timer limpando o timeout.

### `index.js`
- Importação dos módulos (`controls`, `timer`, `sounds`, `elements`).
- Instanciação dos controles, timer e sons.
- Associação dos eventos de clique dos botões às funções corretas dos módulos.
- Controle visual e funcional dos botões de som.
- Integração entre controles, timer e sons para garantir o funcionamento sincronizado.

### `sounds.js`
- Criação dos objetos de áudio para botões, timer e som de fundo.
- Funções para tocar os sons nos momentos certos (pressionar botão, timer terminar).
- Controle do áudio de fundo (play/pause).

---

Essas anotações servem como referência rápida para revisar os conceitos e funcionalidades implementadas neste projeto, incluindo a estrutura e lógica dos arquivos JavaScript.
