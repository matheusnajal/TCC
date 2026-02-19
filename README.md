# Modelagem e Simulação de Corpos e Tecidos Deformáveis em Motores de Jogos

**Autor:** Matheus Najal Cruz

**Instituição:** Universidade de Fortaleza (UNIFOR) - Ciência da Computação

**Ano:** 2026

## Sobre o Projeto

Este projeto de Trabalho de Conclusão de Curso (TCC) investiga e compara métodos geométricos, físicos e híbridos para a simulação de corpos e tecidos deformáveis. O foco é a integração e a avaliação técnica do desempenho dessas simulações em motores de jogos contemporâneos para o desenvolvimento de aplicações gráficas interativas.

## Motores Analisados

A pesquisa avaliou a viabilidade, estabilidade e custo computacional da implementação de *soft body* e *cloth* nas seguintes plataformas:

* **Godot 4:** Utiliza o nó `SoftBody3D` com integração ao Jolt Physics e Bullet Physics.

* **Unity 6:** Análise do componente nativo `Cloth` e soluções custumizadas via *scripts* e *assets* (Como Obi SoftBody).

* **Unreal Engine 5:** Foco nos solucionadores nativos baseados no motor físico Chaos (Chaos Flesh para geometrias volumétricas e Chaos Cloth para tecidos)

* **NVIDIA Omniverse:** Utilização do motor PhysX5, aplicando o Método dos Elementos Finitos (FEM) para *Deformable Bodies* e o sistema *Particle Cloth* para tecidos.

## Casos Experimentais

Foram desenvolvidos dois cenários para estressar os motores de física de cada ferramenta:

1. **Deformação e Acoplamento de Esferas:** Simulação de uma esfera deformável colidindo e se acoplando sobre uma esfera rígida, testando deformação, restituição de volume e estabilidade de colisão.

2. **Simulação de Toalha sobre uma Mesa:** Avaliação da aderência e fluidez de uma malha plana (*cloth*) sobre uma geometria complexa (superfície circular plana), focada no comportamento aerodinâmico e atrito.

## Demonstrações Visuais

> **Nota de Implementação:** Os vídeos (`.mkv`) estão ancorados em imagens de miniatura (`.png`). Clique nas miniaturas para reproduzir os arquivos do repositório. O layout segue o padrão de exibição em colunas agrupadas de duas em duas.

### Godot 4
| Caso 1: Esfera 1 (Bouncing) | Caso 2: Esfera 2 (Acoplamento) |
| :---: | :---: |
| [![Godot Esfera 1](.\images\godot\Esfera1.png)](.\videos\godot\Godot1.mp4) | [![Godot Esfera 2](.\images\godot\Esfera2.png)](.\videos\godot\Godot2.mp4) |
| **Caso 3: Toalha sobre a Mesa** | |
| [![Godot Toalha](.\images\godot\Toalha.png)](.\videos\godot\Godot3.mp4) | |

### Unreal Engine 5
| Caso 1: Esfera 1 (Bouncing) | Caso 2: Esfera 2 (Acoplamento) |
| :---: | :---: |
| [![Unreal Esfera 1](./thumbs/unreal_esfera1.png)](./videos/unreal_esfera1.mkv) | [![Unreal Esfera 2](./thumbs/unreal_esfera2.png)](./videos/unreal_esfera2.mkv) |
| **Caso 3: Toalha sobre a Mesa** | |
| [![Unreal Toalha](./thumbs/unreal_toalha.png)](./videos/unreal_toalha.mkv) | |

### NVIDIA Omniverse
| Caso 1: Esfera 1 (Bouncing) | Caso 2: Esfera 2 (Acoplamento) |
| :---: | :---: |
| [![Omniverse Esfera 1](./thumbs/omni_esfera1.png)](./videos/omni_esfera1.mkv) | [![Omniverse Esfera 2](./thumbs/omni_esfera2.png)](./videos/omni_esfera2.mkv) |
| **Caso 3: Toalha sobre a Mesa** | |
| [![Omniverse Toalha](./thumbs/omni_toalha.png)](./videos/omni_toalha.mkv) | |

### Unity 6
| Caso 1: Esfera 1 (Bouncing) | Caso 2: Esfera 2 (Acoplamento) |
| :---: | :---: |
| [![Unity Esfera 1](./thumbs/unity_esfera1.png)](./videos/unity_esfera1.mkv) | [cite_start]*Inviável via recursos nativos.* O componente `Cloth` não possui parâmetros de elasticidade ou preservação de volume necessários para este comportamento[cite: 558, 560]. |
| **Caso 3: Toalha sobre a Mesa** | |
| [cite_start]*Inviável via recursos nativos.* O componente `Cloth` colide apenas com geometrias esféricas ou capsulares[cite: 565, 566]. | |

---