# Gravidade_particulas


Simulador físico 2D desenvolvido em JavaScript utilizando HTML5 Canvas. O projeto implementa interação gravitacional entre múltiplos corpos, colisões realistas e um sistema de câmera para navegação no espaço simulado.


acesse em <a href =' https://luisfelipe992.github.io/Gravidade_particulas/'>Página de Visualização</a>

---

## 📸 Preview

<img width="1890" height="962" alt="image" src="https://github.com/user-attachments/assets/4545f4e4-81ac-47a1-937d-8a54bb330792" />

---

## 🚀 Funcionalidades

- Gravidade entre corpos (N-body)
- Movimento baseado em posição, velocidade e aceleração
- Sistema completo de colisões:
  - Círculo vs círculo  
  - Retângulo vs retângulo  
  - Círculo vs retângulo  
- Resposta física com:
  - Conservação de momento  
  - Coeficiente de restituição (controle de quique)  
  - Correção de penetração  
- Sistema de estabilização:
  - Remoção de energia residual  
  - Damping  
- Sistema de câmera:
  - Deslocamento do mundo  
  - Seguimento de objetos  
- Efeitos visuais:
  - Base para buraco negro, partículas e distorções  

---

## 🧠 Conceitos Físicos

Este projeto aplica na prática:

- Lei da Gravitação Universal  
- Impulso em colisões  
- Conservação do momento linear  
- Vetores normal e tangencial  
- Detecção e resolução de colisões  
- Diferença entre contato e impacto  

---

## 🏗️ Estrutura

### `Corpo`

Representa um objeto físico:

- posição `(x, y)`
- velocidade `(vx, vy)`
- aceleração `(ax, ay)`
- massa
- tipo (círculo ou retângulo)

Responsável por atualização e renderização.

---

### `Fisica`

Classe estática responsável pela simulação:

- `gravidade(corpos)`
- `colisoes(corpos)` → círculo vs círculo  
- `colisoesRetangulos(corpos)`  
- `colisoesCirculoRetangulo(corpos)`

---

## 🎮 Game Loop

```text
1. Aplicar forças (gravidade)
2. Atualizar corpos
3. Resolver colisões (múltiplas iterações)
4. Renderizar
