# 🖥️ Monitor de Programação v1.0.2

O **Monitor de Programação** é uma ferramenta desktop de alta performance desenvolvida em **Electron** projetada para otimizar o fluxo de trabalho de desenvolvedores web e mobile. O aplicativo monitora arquivos em tempo real e renderiza automaticamente um preview instantâneo do projeto, eliminando a necessidade de dar *F5* ou recarregar o navegador manualmente a cada alteração de código.

Com suporte nativo a projetos estruturados em **HTML estático** e integração simplificada com ambientes locais **PHP (Localhost)**, o sistema analisa as modificações linha por linha e aplica focos visuais dinâmicos diretamente no elemento alterado.

---

## 🚀 Funcionalidades Principais

* **Vigia de Arquivos Inteligente (Chokidar):** Monitoramento contínuo em segundo plano focado apenas nos arquivos do seu projeto (ignorando automaticamente pastas pesadas como `.git` e `node_modules`).
* **Modo Duplo de Preview:**
    * *Modo HTML:* Identifica e abre arquivos locais instantaneamente.
    * *Modo PHP:* Conecta-se à sua porta local (XAMPP, Docker, Wamp) para processar scripts dinâmicos no servidor local.
* **Rastreamento de Alterações Estreito:** O console interno exibe a linha exata que foi modificada, identificando a linguagem e classificando o impacto do código (Estrutural, Estilo, Título, Texto ou Funções).
* **Scroll & Destaque Automático:** Ao salvar uma alteração no seu editor de código, o preview rola suavemente até o elemento alterado e aplica um contorno azul temporário de destaque.
* **Menu de Configurações Integrado:** Sistema de onboarding com tutorial interativo de 5 passos salvos em cache no diretório do usuário para não incomodar após o primeiro acesso.
* **Interface Dark Premium:** Design moderno focado em contraste escuro com detalhes em azul claro, otimizado para evitar a fadiga visual durante longas jornadas de programação.

---

## 🛠️ Arquitetura Técnica

O projeto é baseado no ecossistema do Node.js utilizando os seguintes pilares:

* **Electron:** Framework principal para encapsulamento e execução da aplicação nativa.
* **Chokidar:** Monitor de eventos do sistema de arquivos otimizado, evitando alto consumo de CPU.
* **IPC (Inter-Process Communication):** Comunicação síncrona e assíncrona segura entre o Processo Principal (`main.js`) e a Janela de Renderização (`renderer.js`).
* **Electron Webview:** Tag nativa isolada para renderização segura do preview do projeto monitorado.

---
