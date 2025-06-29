# Chronos Pomodoro

Um **timer Pomodoro** web, construído com **React 19**, **TypeScript** e **Vite**, que ajuda a organizar ciclos de trabalho e descanso de forma simples e eficiente.

---

## 📝 Descrição

O Chronos Pomodoro permite:

- Iniciar ciclos de **25 min** de foco (trabalho) e intercalar com pausas curtas (5 min) e longas (15 min).
- Pausar, interromper ou resetar o ciclo atual.
- Receber notificação sonora ao fim de cada sessão.
- Acompanhar o histórico de tarefas concluídas e interrompidas.
- Customizar os tempos de foco, pausa curta e pausa longa.
- Manter o estado sincronizado com o **localStorage**, permitindo retomar mesmo após fechar o navegador.
- Atualização dinâmica do título da aba com o tempo restante.

---

## 🚀 Tecnologias

- **Framework**: React 19 + Vite
- **Tipagem**: TypeScript
- **State management**: Context API + `useReducer`
- **Web Worker**: `TimerWorkerManager` para contagem de tempo off-thread
- **Data**: `date-fns`
- **UI**:
  - Ícones: `lucide-react`
  - Rotas: `react-router` (v7)
  - Toasts: `react-toastify`
- **Estilos**: CSS modular em `src/styles/global.css` e `src/styles/theme.css`

---

## 📂 Estrutura

```
📦 src
 ┣ 📂 assets
 ┃ ┗ 📂 audios
 ┃   ┗ gravitational_beep.mp3
 ┣ 📂 components
 ┃ ┗ … (UI: botões, listas, formulários)
 ┣ 📂 contexts
 ┃ ┗ TaskContext/  
 ┃     ┣ initialTaskState.ts  
 ┃     ┣ taskActions.ts  
 ┃     ┣ taskReducer.ts  
 ┃     ┗ TaskContextProvider.tsx  
 ┣ 📂 models
 ┃ ┣ TaskModel.ts  
 ┃ ┗ TaskStateModel.ts  
 ┣ 📂 routers
 ┃ ┗ MainRouter.tsx  
 ┣ 📂 utils
 ┃ ┣ formatSecondsToMinutes.ts  
 ┃ ┣ getNextCycle.ts  
 ┃ ┗ loadBeep.ts  
 ┣ 📂 workers
 ┃ ┣ TimerWorkerManager.ts  
 ┃ ┗ timerWorker.js  
 ┣ 📂 styles
 ┃ ┣ global.css  
 ┃ ┗ theme.css  
 ┗ App.tsx
```

---

## ⚙️ Primeiros passos

1. **Pré-requisitos**

   - Node.js 16+
   - npm ou yarn

2. **Instalação**

   ```bash
   # Clone o repositório
   git clone https://github.com/Bruno-Biscaia/chronos-pomodoro.git
   cd chronos-pomodoro

   # Instale as dependências
   npm install
   # ou
   yarn
   ```

3. **Modo desenvolvimento**

   ```bash
   npm run dev
   # abre em http://localhost:5173
   ```

4. **Build para produção**

   ```bash
   npm run build
   ```

5. **Preview da build**

   ```bash
   npm run preview
   ```

---

## ⭐ Funcionalidades

- **Iniciar/Parar**: botão para iniciar e interromper o timer.
- **Reset**: limpar o ciclo atual e histórico.
- **Histórico**: registro de tarefas concluídas e interrompidas, com timestamp.
- **Configurações**: ajustar tempos de foco, pausas curtas e longas.
- **Notificações**: alerta sonoro ao concluir cada sessão.
- **Persistência**: estado salvo no `localStorage` para continuidade.

---

## 🤝 Contribuição

1. Faça um **fork** do projeto
2. Crie uma **branch** para sua feature/bugfix
   ```bash
   git checkout -b feature/minha-nova-funcionalidade
   ```
3. Commit e push
   ```bash
   git commit -m "Descrição da mudança"
   git push origin feature/minha-nova-funcionalidade
   ```
4. Abra um **Pull Request** aqui no GitHub

---

## 📝 Licença

Atualmente não há arquivo de licença neste repositório.\
Se desejar tornar este projeto open-source, adicione um arquivo `LICENSE` (por exemplo, [MIT](https://opensource.org/licenses/MIT)).

---

> Desenvolvido por **Bruno Biscaia**

