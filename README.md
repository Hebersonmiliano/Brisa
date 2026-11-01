# Brisa

Jogo cozy de sobrevivência e crafting em pixel art isométrica, feito em HTML e JavaScript puro (Canvas 2D), sem bibliotecas.

Você chega a uma ilha vazia e, no seu ritmo, colhe recursos, cultiva uma horta, vende no mercado e enfeita a ilha. Não tem combate, nem planta que morre, nem pressa.

## Como jogar

Abra o `index.html` no navegador, ou ative o GitHub Pages neste repositório (Settings → Pages → branch `main`).

| Ação | Teclado | Mouse / toque |
| --- | --- | --- |
| Andar | WASD ou setas | Toque num tile livre |
| Usar ferramenta | Espaço, F ou E | Toque no alvo destacado |
| Trocar ferramenta | 1 a 5 | Toque na barra |
| Trocar semente ou construção | R | Toque no chip acima da barra |
| Mochila / Mercado | B / M | Botões no canto |

**Ferramentas:** Mão (coleta e guarda construções), Enxada (ara a grama), Regador (molha a terra; enche na água), Sementes e Construir.

O jogo salva sozinho no navegador.

## O que já tem (v0.1)

- Ilha gerada por ruído a cada partida, com campina, bosque, colinas e praia
- Horta com nabo e abóbora, que crescem só com a terra regada
- Mercado para vender a colheita e comprar sementes
- Construções: caminho, cerca que se conecta, lanterna, banco, canteiro de flores e casinha de passarinho
- 8 tarefas em sequência que ensinam cada sistema
- Ciclo de dia e noite com lanternas, borboletas e vagalumes

## Próximas versões

| Versão | Conteúdo |
| --- | --- |
| v0.1.5 | Código dividido em módulos ES, save com versão e fila de ações |
| v0.2a | Personagem articulado: rig de 15 peças com animações por keyframes |
| v0.2b | Casa em 6 fases, bancada, forno, interior e móveis |
| v0.3 | Pesca: lago, cais, minigame, 12 peixes e diário |
| v0.4 | Barraca do mercado, fogão e receitas, música e efeitos |
| v0.5 | Quatro estações |
| v0.6 | Ilhota secreta e segundo andar da casa |

O Game Design Document completo descreve cada sistema, os números de balanceamento e o guia de implementação.

## Tecnologia

- Um único `index.html` com CSS e JavaScript embutidos
- Mundo de 48 × 48 tiles, tiles de 32 × 16 px desenhados num buffer de baixa resolução e ampliados sem suavização
- Caminho por BFS em 8 direções, ordem de desenho por diagonal e picking com altura
