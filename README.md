# Modelagem e Simulação de Corpos e Tecidos Deformáveis em Motores de Jogos

**Autor:** Matheus Najal Cruz

**Instituição:** Universidade de Fortaleza (UNIFOR) - Ciência da Computação

**Ano:** 2026

## Sobre o Projeto

Este projeto de Trabalho de Conclusão de Curso (TCC) investiga e compara métodos geométricos, físicos e híbridos para a simulação de corpos e tecidos deformáveis. O foco é a integração e a avaliação técnica do desempenho dessas simulações em motores de jogos contemporâneos para o desenvolvimento de aplicações gráficas interativas.

## Motores Analisados

A pesquisa avaliou a viabilidade, estabilidade e custo computacional da implementação de *soft body* e *cloth* nas seguintes plataformas:

* **Godot 4:** Utiliza o nó `SoftBody3D` com integração ao Jolt Physics e Bullet Physics.

* **Unity 6:** Análise do componente nativo `Cloth` e soluções customizadas via *scripts* e *assets* (como Obi SoftBody).

* **Unreal Engine 5:** Foco nos solucionadores nativos baseados no motor físico Chaos (Chaos Flesh para geometrias volumétricas e Chaos Cloth para tecidos).

* **NVIDIA Omniverse:** Utilização do motor PhysX 5, aplicando o Método dos Elementos Finitos (FEM) para *Deformable Bodies* e o sistema *Particle Cloth* para tecidos.

## Casos Experimentais

Foram desenvolvidos dois cenários para estressar os motores de física de cada ferramenta:

1. **Deformação e Acoplamento de Esferas:** Simulação de uma esfera deformável colidindo e se acoplando sobre uma esfera rígida, testando deformação, restituição de volume e estabilidade de colisão.

2. **Simulação de Toalha sobre uma Mesa:** Avaliação da aderência e fluidez de uma malha plana (*cloth*) sobre uma geometria complexa (superfície circular plana), focada no comportamento aerodinâmico e atrito.

## Resultados e Considerações

A análise comparativa revelou o *trade-off* estrutural entre fidelidade e custo de processamento:

* **Godot 4:** Implementação com processamento leve e rápido, contudo, é a plataforma mais instável devido a *bugs* inerentes ao `SoftBody3D`.

* **Unity:** Inválida para colisões complexas de forma nativa. O componente `Cloth` é eficiente, mas restrito a colisões com formas primitivas esféricas ou de cápsula.

* **Unreal Engine:** Resultados robustos e estáveis. Trata-se de uma opção viável para produção de alta fidelidade, porém o custo computacional exigido (especialmente pelo Chaos Flesh) é elevado.

* **NVIDIA Omniverse:** Qualidade de simulação superior, resolvendo interações e colisões de forma impecável. É, todavia, a ferramenta mais custosa em termos de *hardware*, exigindo compensações como DLSS.

## Documento Completo

Para acessar a pesquisa detalhada, referências teóricas e análises completas de desempenho, faça o download do documento do TCC abaixo:

[📄 Baixar PDF do TCC (TCC_MatheusNajal.pdf)](TCC_MatheusNajal.pdf)