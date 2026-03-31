
## 🧨 CANOON — Jogo de Física com Lançamento de Projetéis

### 🎮 Sobre o Jogo

**CANOON** é um jogo em que você controla um canhão e deve acertar o alvo em diferentes fases ou praticar livremente. 
Com física realista baseada em parábolas, o jogador pode controlar força e direção com o mouse. O jogo inclui:

* 🎯 Modo Livre: pratique seus lançamentos sem restrições.
* 🧩 Modo Fases: enfrente obstáculos progressivos e resolva desafios físicos.
* 📈 Exibição da parábola, pontos de trajetória e equação da função.
* 💥 Detecção de colisão precisa com hitboxes circulares.
* 📋 Popups flutuantes para menus e mensagens (pausa, sucesso, fim de jogo).
* 🖱️ Interface interativa com botões clicáveis.

---

### 🛠️ Como Rodar

#### Pré-requisitos:

* Python 3.10 ou superior
* Biblioteca [pygame](https://pypi.org/project/pygame/)

#### Instalação:

```bash
pip install pygame
pip install sys
pip install math
pip install numpy
```

#### Execução:

```bash
python main.py
```

---

### 📂 Estrutura do Projeto

```
CANOON/
├── main.py                  # Início do jogo (menu principal)
├── modo_livre.py           # Lógica do modo livre
├── modo_fases.py           # Lógica do modo por fases
├── interfaces.py           # Telas de pausa, sucesso e fim de jogo (popups)
├── settings.py             # Tela, fonte, clock e outras configurações globais
├── assets/                 # Pasta opcional com imagens, sons etc.
└── README.md               # Este arquivo
```

---

### 🎓 Conceitos Envolvidos

* **Física de Projetéis:** cálculo da trajetória parabólica com base em velocidade e ângulo.
* **Vetores e Colisão Circular:** colisão entre objetos com base em distância entre centros.
* **Interface Responsiva:** botões com hover e clique, eventos de teclado e mouse.
* **Modularização:** cada parte do jogo está organizada em arquivos separados.

---

### 🚀 To-do Futuro (ideias de expansão)

* 🎨 Tela de seleção de fases
* 🔊 Efeitos sonoros e trilha sonora
* 🧠 Inimigos móveis ou desafios com tempo

---


