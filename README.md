#  CANOON — Jogo de Física com Lançamento de Projéteis

##  Sobre o Jogo

**CANOON** é um jogo educativo em que você controla um canhão para acertar alvos em diferentes fases ou praticar livremente. O objetivo é gamificar o estudo de **equações de segundo grau** e conceitos de **física de projéteis**, permitindo interação e aprendizado prático.

Funcionalidades principais:

*  **Modo Livre:** pratique lançamentos com física realista; trajetória é exibida em tempo real.
*  **Modo Fases:** desafios progressivos focados em acertar alvos e passar de fase.
*  **Exibição de parábola e equação:** função quadrática calculada a partir do ponto inicial, vértice e ponto de impacto.
*  **Detecção de colisão precisa:** hitboxes circulares para interação física realista.
*  **Interface interativa:** menus, popups de pausa e feedback de sucesso.

---

##  Implementação Matemática e Física

A trajetória do projétil é reconstruída a partir de três pontos extraídos da simulação: **ponto inicial**, **vértice** e **ponto final**.

Processo:

1. Conversão do sistema de coordenadas da tela (pixels) para o **plano cartesiano**.
2. Montagem de um sistema linear com os três pontos para calcular os coeficientes da função quadrática `a`, `b`, `c`.
3. Refinamento analítico do vértice para maior precisão.
4. Visualização da parábola em tempo real com pontos-chave e equação exibida.

Além disso, o lançamento considera:

* Vetores de direção usando `atan2`, `cos` e `sin`
* Intensidade baseada na duração do clique
* Gravidade simulada para movimento realista

Esse pipeline permite transformar a simulação física em uma **representação matemática exata**, unindo **programação, física e matemática aplicada**.

---

##  Como Rodar

### Pré-requisitos

* Python 3.10 ou superior
* Biblioteca [pygame](https://pypi.org/project/pygame)

### Instalação

```bash
pip install pygame numpy
```

### Execução

```bash
python main.py
```

---

##  Estrutura do Projeto

```
CANOON/
├── main.py                 # Menu principal
├── modo_livre.py           # Lógica do modo livre
├── modo_fases.py           # Lógica do modo por fases
├── interfaces.py           # Telas de pausa, sucesso e fim de jogo
├── settings.py             # Configurações globais (tela, fonte, clock)
├── assets/                 # Imagens, sons e sprites
├── math_utils.py           # Funções matemáticas (parábola, coordenadas, lançamento)
├── draw_utils.py           # Funções de desenho e visualização
├── game_utils.py           # Funções auxiliares (reset, eventos)
└── README.md               # Este arquivo
```

---

##  Modos de Jogo

###  Modo Livre

Focado em experimentação e aprendizado:

* Simulação completa da física do lançamento
* Geração da equação da trajetória após o impacto

###  Modo Fases

Focado em gameplay e aplicação prática:

* Desafios progressivos com múltiplas fases
* Obstáculos e objetivos dinâmicos
* Aplicação da mecânica de lançamento em cenários variados

---

##  Sistema de Fases e Gameplay

O modo de fases introduz uma camada adicional de complexidade ao projeto, focando na aplicação prática da mecânica de lançamento em cenários dinâmicos.

### Principais características:

* Sistema de progressão com múltiplas fases configuráveis
* Gerenciamento de estado entre fases (reinício, avanço ou retorno ao menu)
* Obstáculos dinâmicos com transformação (escala e rotação)
* Plataforma com hitbox personalizada para colisões específicas
* Detecção de colisão precisa utilizando máscaras (`pygame.mask`)
* Alinhamento dinâmico do canhão com base na posição do mouse
* Reset automático do estado do projétil em caso de falha

Esse modo complementa o aspecto educacional do projeto com elementos de gameplay, reforçando a aplicação prática da física em diferentes cenários.

---

##  Futuro / Possíveis Expansões

*  Tela de seleção de fases
*  Trilha sonora e efeitos sonoros
*  Inimigos móveis e obstáculos com tempo
*  Estatísticas de lançamentos e análise de desempenho

---

##  Competências Desenvolvidas

* Modelagem matemática aplicada e álgebra linear
* Simulação física e vetorial
* Programação modular e limpa em Python
* Visualização gráfica e interface interativa
* Gamificação de conceitos acadêmicos
