# Brisa

Jogo cozy de sobrevivência e crafting em pixel art isométrica, feito em HTML e JavaScript puro (Canvas 2D e Web Audio), sem bibliotecas.

Você chega a uma ilha vazia e, no seu ritmo, corta madeira, minera, cultiva a horta, pesca, constrói sua casa e enfeita tudo. Não tem combate, nem planta que morre, nem pressa.

## Como jogar

Abra o `index.html` no navegador ou ative o GitHub Pages (Settings → Pages → branch `main`, pasta `/ (root)`).

| Ação | Teclado | Mouse / toque |
| --- | --- | --- |
| Andar | WASD ou setas | Toque num tile livre |
| Usar ferramenta | Espaço, F ou E | Toque no alvo destacado |
| Trocar ferramenta | 1 a 8 | Toque na barra |
| Trocar semente ou construção | R | Toque no chip acima da barra |
| Zoom | + e − ou rodinha do mouse | Botões + e − ou pinça com dois dedos |
| Pescar | Espaço para fisgar e segurar | Toque no "!" e segure |
| Mochila / Mercado / Guia da casa | B / M / C | Botões no canto |

O jogo salva sozinho no navegador. Saves da v0.1 são convertidos automaticamente.

## Ferramentas

| # | Ferramenta | Uso |
| --- | --- | --- |
| 1 | Mão | Colhe flores e frutinhas, abre Bancada, Forno e Fogão, martela a obra da casa, guarda construções |
| 2 | Machado | Corta árvores e tocos |
| 3 | Picareta | Quebra pedras e veios de cobre, ferro e cristal |
| 4 | Enxada | Ara a grama; na areia cava argila (perto da água) ou areia |
| 5 | Regador | Molha a terra; enche na água |
| 6 | Sementes | Nabo, milho e abóbora |
| 7 | Vara | Pesca no lago e no mar |
| 8 | Construir | Bancada, forno, cais, placa da casa, cercas, lanternas e móveis |

## O que tem (v0.3)

- **Personagem articulado:** rig de 15 peças com pivôs e animações por keyframes (andar, cortar, minerar, arar, regar, plantar, martelar, lançar, puxar, mostrar o peixe, comemorar), vistas de frente e de costas com espelhamento, piscar de olhos, camisa e chapéu personalizáveis
- **Recursos:** madeira, pedra, cobre, ferro, cristal, argila, areia, fibra, flores e frutinhas
- **Bancada e Forno:** tábuas, iscas, varas, tijolos, telhas e vidro
- **Casa:** placa de terreno 3 × 3, 6 fases de obra (fundação, estrutura, paredes, telhado, porta e janelas, acabamento), fumaça na chaminé e janelas acesas à noite
- **Interior:** cama (dormir pula a noite e salva), mesa, cadeira, tapete, estante com o Diário de Pesca, fogão com receitas, vaso e luminária de cristal
- **Pesca:** lago e mar com 10 espécies por horário, boia, mordida, minigame de faixa verde, tamanhos, recordes e diário
- **Animais:** galinha (ovo), vaca (leite) e ovelha (lã) no Galinheiro e no Estábulo; ração da Bancada ou do Mercado, carinho e corações, Comedouro que alimenta sozinho; gato ou cachorro que segue você e traz presentes
- **Receitas novas no Fogão:** omelete, queijo e bolo de milho
- **Horta:** nabo, milho e abóbora que crescem só com a terra regada
- **Mercado:** venda de tudo o que você produz e compra de sementes e iscas
- **Música:** trilha lo-fi gerada na hora (piano elétrico, baixo, bateria leve, melodia de sininho), mais calma à noite, e efeitos para cada ação
- **31 tarefas** em sequência que ensinam cada sistema
- Ciclo de dia e noite com lanternas, borboletas e vagalumes

## Próximas versões

| Versão | Conteúdo |
| --- | --- |
| v0.3 | Código dividido em módulos ES, barraca do mercado no cais, aquário |
| v0.4 | Quatro estações com culturas e peixes próprios |
| v0.5 | Ilhota secreta e segundo andar da casa |

## Tecnologia

- Um único `index.html` com CSS e JavaScript embutidos
- Mundo de 48 × 48 tiles, tiles de 32 × 16 px desenhados num buffer de baixa resolução e ampliados sem suavização
- Personagem montado por matrizes 2D acumuladas osso a osso; tronco e cabeça ficam retos para manter o pixel art nítido
- Caminho por BFS em 8 direções, ordem de desenho por diagonal e clique que respeita altura e objetos altos
- Áudio 100% sintetizado com Web Audio API, sem arquivos de som
