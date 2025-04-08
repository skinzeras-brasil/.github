# 🔰 LEIA ISSO PRIMEIRO: FAQ da Oficina de CS2 para novatos


E aí, pessoal! Fiz esse post pra responder algumas perguntas que tão aparecendo direto aqui no subreddit com o lançamento do CS2. Aquele FAQ antigo [ FAQ Post ] tá ficando desatualizado com a mudança de engine do Source do CS:GO pro Source 2, então vai precisar ser reescrito em algum momento.

[FAQ da Valve sobre acabamentos de armas](https://www.counter-strike.net/workshop/workshopfaq#weapons) pode responder algumas das suas dúvidas, mas algumas perguntas recentes não estão lá, então vou tentar respondê-las aqui.

## Quanto os criadores de skins ganham?
Não posso revelar meus ganhos, mas quem tem um design escolhido pra entrar no jogo pode esperar uma grana bem confortável. Os designers que aparecem em cada case recebem uma porcentagem de cada chave vendida. (Também não posso dizer quanto é essa porcentagem) Se você precisa de dinheiro urgente, criar skins do Counter-Strike não é um esquema "fica rico rápido". As chances de sucesso são muito baixas pra quem tá começando, como explico na próxima pergunta:

## Quais são as chances do meu design ser aceito?
As chances são, pra ser franco, bem ruins. Pra começar, fazer skins é [ [trabalho especulativo ]: quer dizer que, apesar da recompensa poder ser boa, existe uma grande chance do seu trabalho nunca ser adicionado ao jogo, e você não ser compensado pelo tempo e esforço investidos. Dois fatores principais explicam porque as chances são tão baixas:

- Criar skins pro Counter-Strike é muito bem pago e a barreira pra entrada é baixa, então muita gente tenta, e isso significa que é difícil se destacar.

- Artistas com histórico de sucesso criando skins são pagos o suficiente com os royalties pra continuar trabalhando em tempo integral: eles conseguem aprimorar seu trabalho sem sofrer muito com o impacto de criar coisas que nunca vão render um centavo. Muitos dos "workshoppers" mais populares já enviaram centenas de designs de alta qualidade, qualquer um deles poderia ser escolhido, mas a grande maioria não será.

Cases são adicionados de forma irregular, cerca de quatro por ano em média. Normalmente, eles apresentam 17 designs da comunidade. Normalmente, a maioria das skins selecionadas são de designers de skins experientes e bem-sucedidos.

__Se você precisa de dinheiro com urgência, criar skins do Counter-Strike é uma péssima maneira de ganhar__. Suas chances são incrivelmente baixas, a menos que você já tenha habilidades consideráveis de arte e design, e mesmo assim as chances não são boas. Conheço artistas que trabalham com skins do Counter-Strike há quase uma década e não foram selecionados, e vários que trabalharam por anos antes de serem incluídos. Se você precisa do dinheiro, não perca seu tempo fazendo skins do Counter-Strike, seria melhor usar esse tempo pra ganhar a vida. Na minha opinião, é melhor encarar o design de skins como um hobby com um pequeno potencial de recompensa do que como uma carreira séria.

## Como eu aprendo a fazer skins do CS2 e qual software devo usar?
Bom, se você não desanimou, a primeira coisa que você deve fazer é ler [o guia da Valve](https://www.counter-strike.net/workshop/workshop), em particular o [Guia de Acabamentos de Armas](https://www.counter-strike.net/workshop/workshopfinishes) e o [Guia de Estilo](https://www.counter-strike.net/workshop/workshopstyleguide).

A resposta simples é que, para ter um bom entendimento de como fazer skins, você deve desenvolver conhecimento em modelagem e texturização 3D, em particular texturização para [PBR (Physically based rendering)](https://www.youtube.com/watch?v=a4dURVZEi3E) usando um fluxo de trabalho de metalicidade-rugosidade. Recomendo aprender 3D em vez de apenas texturização porque o pipeline de arte 3D moderno depende muito da arte 3D. O baking de high poly para low poly é a base sobre a qual muitas ótimas skins são construídas.

Para iniciantes em modelagem 3D, sugiro usar [Blender](https://www.blender.org/), que é gratuito e bem documentado online. [Blender Guru](https://www.youtube.com/@blenderguru) tem uma série popular, mas existem muitos outros canais com guias semelhantes que podem ser mais do seu agrado. Existem outros pacotes de software 3D: se um deles for mais do seu agrado, provavelmente será bom para trabalhar.

Para texturização, eu e a maioria dos outros designers de skins que conheço usamos [Substance 3D Painter](https://store.steampowered.com/app/2199970/Substance_3D_Painter_2023/). É o padrão da indústria para artistas de jogos e é de longe o software de texturização mais desenvolvido que conheço. Acredito que a texturização também seja possível usando o Blender, no entanto, o Blender carece da maioria das funcionalidades e recursos de qualidade de vida que você encontrará no Painter. Outros pacotes de texturização, incluindo o 3D-Coat, também foram populares para a criação de skins do CS:GO. O Photoshop é recomendado, embora outros pacotes de edição de imagens como o Affinity Photo ou o GIMP possam oferecer grande parte da mesma funcionalidade.

## Como funciona a seleção de skins? Existe alguma maneira de saber se minha skin está sendo considerada?
O processo de seleção é basicamente a Valve escolhe as skins que eles gostam, e então eles as adicionam a um case de armas, lançado com uma atualização do jogo. Não há como saber se sua skin será adicionada, ou mesmo se está sendo considerada - se for aceita, você descobrirá no momento em que a atualização que a contém for lançada, seja olhando as notas do patch ou por e-mail da Valve.

## Por que meu design não está aparecendo em certas partes da arma?
Leia esta parte do [guia técnico](https://www.counter-strike.net/workshop/workshopfinishes#durability). Você precisa alterar seu canal alfa e exportar como um arquivo .tga de 32 bits.

## Por que meu design não parece correto na arma?
Se seu design não se alinha da mesma forma nas ferramentas da oficina como faz no seu software de texturização, é possível que você esteja usando os modelos de armas do CS:GO em vez dos do CS2. Você precisa usar os modelos de armas do __CS2__ da [página de recursos da oficina](https://www.counter-strike.net/workshop/workshopresources) __NÃO__ os materiais da bancada listados lá. Não sei por que a Valve deixou isso lá, não é mais possível publicar skins para os modelos antigos. Se você desenvolveu um design para os modelos antigos, azar o seu, precisará ser refeito para o novo modelo.

Se este não for o motivo, certifique-se de que seus intervalos de deslocamento X e Y e os valores de rotação estejam definidos como 0, sua escala de textura esteja definida como 1 e "ignorar escala de tamanho da arma" esteja marcado.

## Por que estou recebendo o erro "Resource Compile Items: Failed"?
Possíveis razões:

- Suas texturas não são quadradas com uma potência de dois como resolução de cada lado (como 1024x1024, 2048x2048 ou 4096x4096 pixels)

- Suas texturas têm um espaço no nome do arquivo: use sublinhados em vez de espaços ("_")

- Seus drivers de GPU precisam ser atualizados isso foi um problema em placas AMD algum tempo atrás

Se nenhuma dessas for a causa, reexportar suas texturas com um nome diferente pode ajudar a resolver o problema.

## Qual resolução devo usar para minha skin? Por que minha skin parece ter baixa resolução no jogo?
Idealmente, você deve projetar em uma resolução de 4K (4096 pixels) ou superior para Skins. As ferramentas da oficina irão limitar a resolução a 2K (2048px) para a pré-visualização no jogo, portanto, você pode notar uma aparência mais pixelada, de baixa resolução ao testar seu design. Skins adicionadas recentemente têm texturas 4K nos arquivos do jogo, portanto, é recomendado usar texturas .tga de 4K em sua submissão.

Os adesivos adicionados recentemente parecem ter apenas 1k (1024px) nos arquivos do jogo, e também são limitados a essa resolução pelas ferramentas da oficina.

## Por que estou recebendo tão poucas visualizações e votos na minha submissão na oficina?/Por que minha submissão não está aparecendo na página inicial da oficina?
Você precisa preencher suas informações de pagamento - o link está na sua página da oficina. Antes de fazer isso, sua submissão só será visível para pessoas que visitarem o link diretamente.

## Onde encontro modelos para granadas/facas/luvas?
Submissões para skins de granadas, facas e luvas provavelmente nunca serão aceitas pela Valve, então elas não são permitidas neste subreddit. No entanto, se você precisar delas por algum motivo, você pode extrair as malhas dos arquivos do jogo com [ Source2Viewer], elas estão em pak01_dir.vpk.

Autor: [Ezikyl](https://www.reddit.com/user/Ezikyl_/)
Fonte: [Reddit](https://www.reddit.com/r/csworkshop/comments/16xjrn8/read_this_first_cs2_workshop_faq_for_newcomers/?rdt=54025)
