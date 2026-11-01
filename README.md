# Reino Medieval RTS — base jogável 0.2.0

Projeto Android original, Kotlin + WebView + Canvas 2D, sem Unity e sem API paga. Orientado a celulares intermediários como o Samsung Galaxy M31. A tela do jogo é horizontal.

## O que esta versão implementa
- Mapa 2D interativo com terreno, rio, caminhos, construções, tropas, inimigos, barras de vida e projéteis.
- Economia com ouro, madeira, pedra, ferro, comida e cristal; produção periódica por casas, fazendas, minas, acampamentos madeireiros e porto.
- Catálogo de construções: castelo, casa, fazenda, acampamento madeireiro, mina, mercado, quartel, arquearia, estábulo, oficina de cerco, torre arcana, academia, forja, templo, muralha, portão, torre de guarda, torre elemental, celeiro, armazém, porto, estaleiro, covil do dragão, salão dos gnomos e santuário élfico.
- Unidades: trabalhador, soldado, arqueiro, cavaleiro, lanceiro, magos de fogo/gelo/eletricidade, curandeiro, catapulta, aríete e dragão; inimigos duende, gnomo e ogro.
- Quatro eras com custos de evolução e requisitos de desbloqueio.
- Oficina com fila de fabricação de espada, arco, armadura, poção, essência elemental, flechas, runas e kit de catapulta.
- Pesquisa de agricultura, alvenaria, metalurgia, balística, estudos arcanos, medicina, logística e conhecimento dracônico.
- Combate automático, projéteis, dano, movimento por toque, defesa de construções e ondas de invasores.
- Missões introdutórias, pausa e salvamento local.

## Limitações importantes da versão 0.2.0
Esta é uma base de desenvolvimento jogável, não um RTS comercial completo. A campanha ainda é uma sandbox com objetivos iniciais; pathfinding, animações de sprites, mapas gerados, balanceamento, áudio, tutorial completo, IA estratégica avançada e testes em aparelhos reais ainda precisam ser desenvolvidos.

**Multiplayer:** o menu apresenta o modo online como planejado, mas não há servidor de partidas conectado nesta versão. Multiplayer real exige backend de salas, autenticação, sincronização autoritativa e infraestrutura de rede. Não é simulado como se estivesse funcionando.

**Compatibilidade:** o código foi verificado sintaticamente com Node.js (`node --check`). Isso não substitui a compilação Gradle nem testes de instalação e desempenho no Galaxy M31.

## Gerar APK pelo GitHub
1. Crie um repositório vazio no GitHub.
2. Extraia este ZIP e envie o conteúdo da pasta `ReinoMedievalRTS` para a raiz do repositório.
3. Abra **Actions** e execute **Build Reino Medieval RTS APK** (ou faça push na branch `main`).
4. Quando a execução terminar, baixe o artefato `ReinoMedievalRTS-debug-apk`.
5. Extraia o artefato e instale `app-debug.apk` no Android. Autorize a instalação pelo gerenciador de arquivos se o Android solicitar.

## Abrir no Android Studio
Abra a pasta como projeto Gradle, usando JDK 17 e Android SDK 35. Execute `gradle assembleDebug`.

## Controles
- Menu: abra Construções, Exército, Oficina, Tecnologias, Missões ou Online.
- Construções: escolha uma construção no catálogo e toque em um espaço livre do mapa.
- Exército: toque numa unidade para recrutá-la (o edifício necessário precisa existir).
- Movimento: toque numa tropa no mapa e depois no destino.
- Ataque: selecione uma tropa e toque num inimigo.
- Salvar: grava o estado local no aparelho.
