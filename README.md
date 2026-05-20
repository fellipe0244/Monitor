# 🖥️ Monitor de Programação v1.0.2

O **Monitor de Programação** é uma ferramenta desktop de alta performance desenvolvida em **Electron** projetada para otimizar o fluxo de trabalho de desenvolvedores web e mobile. O aplicativo monitora arquivos em tempo real e renderiza automaticamente um preview instantâneo do projeto, eliminando a necessidade de dar *F5* ou recarregar o navegador manualmente a cada alteração de código.

Com suporte nativo a projetos estruturados em **HTML estático** e integração simplificada com ambientes locais **PHP (Localhost)**, o sistema analisa as modificações linha por linha e aplica focos visuais dinâmicos diretamente no elemento alterado.

---

## 🚀 Funcionalidades Principais

* **Vigia de Arquivos Inteligente (Chokidar):** Monitoramento contínuo em segundo plano focado apenas nos arquivos do seu projeto (ignorando automaticamente pastas pesadas como `.git` e `node_modules`).
* **Modo Duplo de Preview:**
    * *Modo HTML:* Identifica e abre arquivos locais instantaneamente.
    * *Modo PHP:* Conecta-se à sua porta local (XAMPP, Docker, Wamp) para processar scripts dinâmicos no servidor local.
* **Identificador de extensao:** O programa identifica automaticamente, as extensoes (java, java script, python, php, css, html, powershell para linhas de comando) - em desenvolvimento outras extensoes. 
* **Rastreamento de Alterações Estreito:** O console interno exibe a linha exata que foi modificada, identificando a linguagem e classificando o impacto do código (Estrutural, Estilo, Título, Texto ou Funções).
* **Scroll & Destaque Automático:** Ao salvar uma alteração no seu editor de código, o preview rola suavemente até o elemento alterado e aplica um contorno azul temporário de destaque.
* **Menu de Configurações Integrado:** Sistema de onboarding com tutorial interativo de 5 passos salvos em cache no diretório do usuário para não incomodar após o primeiro acesso.
* **Interface Dark Premium:** Design moderno focado em contraste escuro com detalhes em azul claro, otimizado para evitar a fadiga visual durante longas jornadas de programação.

---

## Download >>> https://github.com/fellipe0244/Monitor/releases/tag/version 

## Images 

* **Tutorial:**
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/a47f7af5-8e89-41c0-8230-f88273ed3ee9" />

* **Modo Preview HTML e PHP(se tiver com o localhost ok):**
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/bbf53267-270c-4b13-9ffb-6f3efaba81d1" />
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/ad90a669-abf0-4632-8410-cc1164dce268" />
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/0071416d-3a64-4279-a4f0-63130c5eaa27" />

* **Modo Inspecionar ainda em desenvolvimento:**
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/6aaa3c04-e104-4055-bc32-979f0ce7189c" />
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/17899794-c82e-4324-b818-e1b05ea902e5" />

* **Possibilidade de utilizar com Pastas de Projetos Locais e Externos (File Server, Nuvens em Geral):**
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/e8de34dd-2f85-492e-9a50-43ec5ae73494" />

* **Nas extensoes de arquivos, Java, JS, Python, e PowerShell, um Preview exclusivo, está sendo desenvolvido:** No momento ainda não é exibido nada no lado direito ao monitorar arquivos com essas extensoes.
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/9ad5b2a8-5133-4627-8118-b2482e53d467" />
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/ddf9d3da-8cdd-4dc1-9dd7-b774e2e0597c" />
<img width="60%" alt="image" src="https://github.com/user-attachments/assets/09d47cc0-bb06-46a3-9303-7390c96e394d" />

## 🛠️ Arquitetura Técnica

O projeto é baseado no ecossistema do Node.js utilizando os seguintes pilares:

* **Electron:** Framework principal para encapsulamento e execução da aplicação nativa.
* **Chokidar:** Monitor de eventos do sistema de arquivos otimizado, evitando alto consumo de CPU.
* **IPC (Inter-Process Communication):** Comunicação síncrona e assíncrona segura entre o Processo Principal (`main.js`) e a Janela de Renderização (`renderer.js`).
* **Electron Webview:** Tag nativa isolada para renderização segura do preview do projeto monitorado.

---
