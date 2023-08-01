# Web3Brasil: Curso Rápido sobre Finanças Descentralizadas (DeFi)

Este guia é uma versão resumida do [Guia para Finanças Descentralizadas](https://finematics.com/guide-to-decentralized-finance/) da Finematics. **Eu não sou o autor dos guias originais e utilizei muitas imagens deles**. Também utilizei a estrutura de progressão do guia, mas incluí alguns conceitos extras para garantir que os leitores possam entender completamente a DeFi.

A maioria dos conceitos foi descrita inicialmente pelo GPT-3 AI após alimentá-lo com o artigo completo da Finematics e pedir um "resumo em termos leigos". Em seguida, revisei os textos com a ajuda do Grammarly e adicionei quaisquer detalhes extras que possam ajudar na compreensão do conceito. Foi divertido criar isso e espero que seja uma leitura interessante!

Se você gostar deste conteúdo, siga o criador original de todos os guias usados para produzir este resumo:

- https://twitter.com/finematics
- https://www.youtube.com/c/finematics

E também me siga no Twitter, pois estou sempre explorando e escrevendo sobre DeFi, e mais frequentemente sobre o protocolo [yearn](https://twitter.com/iearnfinance), pois sou um colaborador lá:

- https://twitter.com/MarcoWorms

# Introdução aos Conceitos Básicos de Blockchain

A DeFi acontece principalmente em blockchains, então é importante entender a história e os conceitos básicos dessa tecnologia:

- O primeiro uso popular da tecnologia blockchain surgiu com o Bitcoin em 2009.
- O Bitcoin utilizou a blockchain para criar uma "moeda descentralizada + livro-razão".
- Isso é o que eu quero dizer com livro-razão: uma tabela que registra quanto dinheiro entra e sai de cada conta:
![](https://i.imgur.com/KkL9UOo.png)
- "Descentralizado" nesse contexto significa que qualquer pessoa pode usar esse produto e qualquer pessoa também pode ajudar a manter sua infraestrutura.
    - Qualquer pessoa pode ser um usuário: um usuário pode enviar BTC para outro usuário (há uma taxa para cada transação).
    - Qualquer pessoa pode ser um minerador: um minerador participa do processo de validação das transações dos usuários (e recebe taxas de transação por isso).
- Então, o Bitcoin:
    - criou um novo tipo de dinheiro (BTC).
    - anexou um livro-razão que não pode ser manipulado quando as transações são liquidadas.
    - estabeleceu um fluxo de incentivos para garantir que as pessoas que executam a infraestrutura recebam dinheiro por fazê-lo, garantindo a segurança da rede para o futuro.
- Mas o Bitcoin não permitia que [Contratos Inteligentes](#Contratos-Inteligentes-fonte) acontecessem.
- O Ethereum foi lançado em 2015.
    - era um clone do Bitcoin, mas tinha contratos inteligentes.
    - a moeda que ele criou é chamada de ETH.
    - cada transação, incluindo a interação com contratos inteligentes, tem uma taxa cobrada em ETH (assim como o BTC tem taxas de transação).
- Desde então, o Ethereum tem sido um empreendimento muito bem-sucedido, a DeFi possui mais de $55 bilhões circulando em seus protocolos ([fonte DefiLLama](https://defillama.com/)), e o valor de todas as criptomoedas combinadas já atingiu a magnitude dos trilhões ([fonte CMC](https://coinmarketcap.com/charts/)).

# Novato em DeFi

Este é o nosso primeiro nível, perfeito para iniciantes. Se você já ouviu falar sobre finanças descentralizadas antes, mas todos os conceitos e terminologia parecem um pouco avassaladores - é aqui que você começa.

## O que são Finanças Descentralizadas? ([fonte](https://finematics.com/guide-to-decentralized-finance/))

![](https://i.imgur.com/SrIyP2o.png)

A DeFi é um movimento que visa criar um novo sistema financeiro aberto a todos e que não exija a confiança em intermediários como bancos. Para alcançar isso, a DeFi depende muito da criptografia, blockchain e contratos inteligentes.

O ecossistema da DeFi é composto por várias áreas principais, sendo as principais: Empréstimos e Empréstimos, Moedas Estáveis, Exchanges Descentralizadas, Derivativos, Negociação com Margem e Seguros.

## Carteiras DeFi ([fonte](https://finematics.com/top-3-defi-wallets-for-2021/))

![](https://i.imgur.com/NoZEbGT.png)

As carteiras permitem enviar, receber e armazenar criptomoedas.

Existem muitas carteiras DeFi disponíveis no mercado, cada uma com seu próprio conjunto de recursos, vantagens e desvantagens. As opções mais populares são Metamask, Ledger e Argent:

- [Ledger](https://www.ledger.com/) é uma carteira de hardware que oferece um alto grau de segurança para os ativos digitais dos usuários. No entanto, requer um dispositivo de hardware separado e não é tão conveniente de usar quanto outras carteiras. Você pode conectar carteiras Ledger ao Metamask para usá-las no navegador.
- [Metamask](https://metamask.io/) permite que os usuários interajam com aplicativos DeFi. Bom para criar novas "carteiras quentes" que não mantêm fundos o tempo todo, mas podem ser usadas para testar coisas sem expor sua carteira principal.
- [Argent](https://www.argent.xyz/) é uma carteira móvel não custodial integrada a vários protocolos DeFi. Ele usa um modelo de recuperação social que não requer uma frase de recuperação.

Vale mencionar dois aplicativos que facilitam a gestão de uma carteira DeFi: [Zapper](https://zapper.fi/) e [Zerion](https://zerion.io/).

Tecnicamente, uma carteira é um par de:
- Uma chave **pública**, conhecida como seu endereço público
- Uma chave **privada**, que quem a possui pode agir como proprietário do endereço público

E um bom conceito a ter em mente é que nada está dentro da sua carteira. Você marca coisas na blockchain com seu endereço **público** e, depois de marcadas como suas, somente você pode alterar o endereço usando sua chave **privada**. Todas as carteiras mencionadas ajudam a manter sua chave privada segura, mas o conselho mais sensato hoje para qualquer usuário médio de DeFi é: **use carteiras de hardware**.

![](https://i.imgur.com/WaRuf18.png)

## Contratos Inteligentes ([fonte](https://finematics.com/smart-contracts-explained/))

![](https://i.imgur.com/PPzHFll.png)

Contratos inteligentes são trechos de código que podem ser executados automaticamente e de forma determinística. O código do contrato inteligente geralmente é armazenado e executado na blockchain para torná-lo confiável e seguro. Os contratos inteligentes também têm a capacidade de receber, armazenar e enviar fundos e até mesmo chamar outros contratos inteligentes.

Os contratos inteligentes visam remover o fator humano da tomada de decisões. O fator humano muitas vezes se mostra o elemento mais propenso a erros e menos confiável dos contratos tradicionais.

O [Ethereum](https://ethereum.org/en/) é um bom exemplo de uma blockchain que suporta contratos inteligentes e permite que os programadores os implementem. Os contratos inteligentes podem ser escritos em uma linguagem de programação chamada Solidity, que foi criada especificamente para esse fim. No Ethereum, todos os contratos inteligentes implantados são imutáveis. Isso significa que, uma vez implantados, eles não podem ser modificados. Além do Solidity, os programadores podem usar outras linguagens para criar contratos inteligentes no Ethereum, como [Vyper](https://github.com/vyperlang/vyper) ou [Huff](https://huff.sh/).

Um contrato inteligente no Ethereum é uma carteira com funções embutidas:

<img src="https://i.imgur.com/6qH5Wto.png" width="400"/>

Embora o Ethereum seja atualmente a plataforma de contrato inteligente mais popular, não é a única com alguns concorrentes. Alguns deles são [Solana](https://solana.com/), [Tezos](https://tezos.com/), [Tron](https://tron.network/), mas nem todos compartilham as mesmas características.

## ERCs ([fonte](https://ethereum.org/en/eips/))

ERC (Ethereum Request for Comments) é um processo formal para propor melhorias na rede Ethereum. Ele permite que qualquer pessoa envie uma proposta de como a rede deve ser melhorada e, em seguida, dá à comunidade a chance de discutir os méritos da proposta e votar se ela deve ou não ser implementada. Se uma Proposta de Melhoria (EIP) receber apoio suficiente da comunidade, ela se torna um ERC.

### ERC20

O padrão [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) define um conjunto de regras sobre como os tokens no blockchain Ethereum devem ser construídos. Essas regras incluem como os tokens podem ser transferidos, como eles são aprovados e como os dados sobre os tokens são armazenados na blockchain. O padrão também define como os tokens interagem entre si na blockchain Ethereum. O padrão ERC20 é usado pela maioria dos tokens populares, como USDC, USDT, DAI, CRV, YFI, UNI, SUSHI e muitos outros.

## Uniswap (Exchanges Descentralizadas) ([fonte](https://finematics.com/uniswap-uni-token-explained/))

![](https://i.imgur.com/JnvmANj.png)

[Uniswap](https://app.uniswap.org/#/swap) é um protocolo para a troca descentralizada de tokens na blockchain Ethereum. O protocolo Uniswap é implantado como um conjunto de contratos inteligentes e é completamente descentralizado, sem permissões e resistente à censura. O Uniswap é construído com base no conceito de [pools de liquidez](#Pools-de-Liquidez-fonte) e formadores de mercado automatizados, ou, para ser preciso, um formador de mercado de produto constante.

A primeira versão do protocolo foi lançada em 2 de novembro de 2018. O protocolo rapidamente ganhou muita tração, o que resultou em um investimento inicial que permitiu à equipe do Uniswap trabalhar na segunda versão do protocolo, que introduziu a implementação atual de pools de liquidez usadas em muitos protocolos DeFi.

## Empréstimos e Empréstimos ([fonte](https://finematics.com/lending-and-borrowing-in-defi-explained/))

![](https://i.imgur.com/QhLj9WZ.png)

Os empréstimos e empréstimos podem ser feitos na DeFi de forma completamente descentralizada e sem permissões, mantendo a custódia total sobre suas moedas. Nos empréstimos da DeFi, as taxas operacionais são recalculadas em cada mudança de estado da blockchain Ethereum, o que proporciona taxas de juros variáveis que podem mudar bastante dependendo da demanda por empréstimos e empréstimos de determinados tokens. A quantidade que pode ser emprestada depende de 2 fatores principais:
- O primeiro é a quantidade de fundos disponíveis para serem emprestados em um mercado específico.
- O segundo é qual é o fator de colateral dos tokens fornecidos pelo mutuário.

O fator de colateral determina quanto pode ser emprestado com base na qualidade do colateral. Se um usuário decide pegar emprestado fundos, o valor do montante emprestado deve sempre ser menor que o valor do colateral fornecido multiplicado pelo seu fator de colateral. Se essa condição for atendida, não há limite para quanto tempo um usuário pode pegar emprestado fundos. Duas famosas plataformas de empréstimos DeFi são [AAVE](https://aave.com/) e [Compound](https://compound.finance/).

# Aprendiz de DeFi

Neste nível, você se sente confortável com todos os conceitos incluídos no nível de Novato em DeFi e está pronto para se aprofundar no futuro das finanças!

## Moedas Estáveis ([fonte](https://stablecoins.wtf/resources/the-relevance-of-stablecoins))

As moedas estáveis são tokens que afirmam manter uma relação de valor de 1:1 com outra moeda. Cada moeda estável precisa equilibrar os riscos entre:

- Descentralização (mais centralizado = mais risco de congelamento de fundos)
- Estabilidade de preço (preço instável compromete o propósito do produto e perde a confiança da comunidade)
- Custo para emissão (se for muito caro, todas as operações financeiras usando essa moeda se tornam mais caras)

Existem aproximadamente três tipos de moedas estáveis, cada uma focando mais em alguns dos problemas acima:
- **Lastreadas por moeda fiduciária (Exemplos: [USDC](https://www.circle.com/en/usdc), [USDT](https://tether.to/), [BUSD](https://www.binance.com/en/busd)):** essas moedas estáveis são as mais proeminentes e usadas. Elas são lastreadas 1:1 por dólares reais e exigem que contas bancárias detenham dólares para lastrear a emissão das moedas estáveis. Essa operação pode ser replicada para qualquer outro ativo, por exemplo, o wBTC é uma moeda estável de BTC dentro da rede Ethereum, então você pode usar BTC em operações DeFi.
- **Lastreadas por criptomoedas (Exemplo: [DAI](https://makerdao.com/en/), [MIM](https://abracadabra.money/), [LUSD](https://www.liquity.org/)):** essas moedas estáveis são lastreadas por outros ativos digitais, como BTC, ETH. Criadas por meio da operação de [Empréstimos e Empréstimos](#Empréstimos-e-Empréstimos-fonte).
- **Moedas estáveis algorítmicas (Exemplo: [FRAX](https://frax.finance/)):** implementaram um algoritmo que equilibra a oferta e demanda da moeda estável para manter a estabilidade de preço.

## Pools de Liquidez ([fonte](https://finematics.com/liquidity-pools-explained/))

<img src="https://i.imgur.com/FcfyOTW.png" width="600"/>

As Pools de Liquidez (LPs) são contratos inteligentes que possuem uma determinada quantidade de 2 tokens diferentes e permitem que os usuários troquem esses tokens diretamente entre si. Esse processo é completamente descentralizado, portanto, não há necessidade de uma exchange centralizada que normalmente detém os tokens e facilita a negociação.

Sempre que um usuário deseja trocar um token por outro, ele simplesmente vai para uma pool de liquidez que possui esses 2 tokens e realiza uma negociação. A pool de liquidez usa um algoritmo especial chamado formador de mercado automatizado (AMM) para determinar o preço dos tokens na pool e facilitar as negociações. Todo esse processo geralmente é bastante rápido e geralmente é mais barato do que usar uma exchange centralizada.

Qualquer usuário pode se tornar um provedor de liquidez fornecendo tokens para a pool na mesma proporção em que eles existem atualmente, ou também pode criar uma nova LP fornecendo um novo par de tokens. Se uma pool tiver, por exemplo, 10 ETH e 50.000 DAI, significa que se eu quiser adicionar 1 ETH, também tenho que adicionar 5.000 DAI para me tornar um provedor dessa pool. Os provedores recebem parte das taxas de negociação, outra parte vai para o protocolo da [DEX](#Uniswap-Exchanges-Descentralizadas-fonte) (por exemplo, [Uniswap](#Uniswap-Exchanges-Descentralizadas-fonte)) que permite que os provedores de liquidez criem as pools e os usuários as encontrem para negociar.

Como as pools de liquidez são apenas contratos inteligentes, elas podem ser modificadas para conter mais de 2 tokens ou ter um algoritmo de precificação diferente que funcione melhor com determinados ativos. Isso é o que o [Curve](https://curve.fi/) fez, otimizou o algoritmo da LP para pools feitas de 2 stablecoins do mesmo ativo e se tornou um dos protocolos DeFi mais bem-sucedidos.

## Perda Temporária ([fonte](https://finematics.com/impermanent-loss-explained/))

A perda temporária é uma perda temporária de fundos que ocorre ao fornecer liquidez. Geralmente é explicada como a diferença entre manter um ativo versus fornecer liquidez para esse ativo. A perda temporária é geralmente observada em pools de liquidez padrão, onde o provedor de liquidez (LP) precisa fornecer ambos os ativos na proporção correta, e um dos ativos é volátil em relação ao outro, por exemplo, em uma pool Uniswap DAI/ETH 50/50.

Se o ETH valorizar, a pool precisa confiar em arbitragistas (usuários que realizam negociações lucrativas até que a proporção da pool corresponda aos preços de mercado) para garantir continuamente que o preço da pool reflita o preço real para manter o mesmo valor de ambos os tokens na pool. Isso leva a uma situação em que o lucro do token que se valorizou é retirado do provedor de liquidez. Nesse ponto, se o LP decidir retirar sua liquidez, a perda temporária se torna permanente.

![](https://i.imgur.com/bmUE5M4.png)

## Farming de Rendimento ([fonte](https://finematics.com/yield-farming-explained/))

O farming de rendimento, essencialmente, é uma forma de maximizar a taxa de retorno do capital alavancando diferentes protocolos DeFi. Os farmers de rendimento tentam buscar o maior rendimento trocando entre várias estratégias diferentes. As estratégias mais lucrativas geralmente envolvem pelo menos alguns protocolos DeFi, como Compound, Curve, Synthetix, Uniswap ou Balancer. Se a estratégia não funcionar ou se houver uma estratégia melhor disponível, os farmers de rendimento movem seus fundos. Eles podem, por exemplo, mover os fundos entre diferentes protocolos ou trocar algumas de suas moedas por outras que estão gerando mais rendimento no momento. No mundo do farming de rendimento, esse procedimento às vezes é chamado de rotação de culturas.

![](https://i.imgur.com/lWroYNw.png)

## Yearn Finance e Token YFI ([fonte](https://finematics.com/yearn-finance-and-yfi-explained/))

[yearn.finance](https://yearn.finance/#/portfolio) é um otimizador de [farming de rendimento](https://hackmd.io/J7kGRZNDT7KHAhy0l2fh7Q#Farming-de-Rendimento-fonte) que automatiza o processo de escolha dos protocolos de empréstimos que pagam mais para seus stablecoins na versão 1. O protocolo permite que você deposite seus stablecoins em uma pool e receba uma versão que rende juros chamada de yvToken. Atualmente, a versão 2 permite várias estratégias de rendimento diferentes para cada vault.

O [YFI](https://etherscan.io/token/0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e) é o token de governança do [protocolo yearn](https://docs.yearn.finance/getting-started/intro). Ele foi distribuído aos usuários do protocolo para decidir sobre o futuro do protocolo. Hoje, o yearn é mantido por um grupo de pessoas em todo o mundo, sem liderança centralizada, governado pelo token YFI.

![](https://i.imgur.com/xRwHpVU.png)

### Vaults Yearn: Vault ETH Explained ([fonte](https://finematics.com/yearn-vaults-eth-vault-explained/))

Em resumo, o Yearn ETH Vault gera rendimento pegando emprestado DAI do MakerDAO e usando-o para fornecer liquidez à pool Curve Y. Isso resulta em recompensas com tokens CRV, que são então vendidos por ETH. O ETH é usado para pagar as taxas de transação e os juros do empréstimo DAI. O restante do ETH é reinvestido no Vault.

![](https://i.imgur.com/wTOC4EM.png)

# Mestre de DeFi

Os conceitos incluídos em Novato em DeFi e Aprendiz de DeFi parecem fáceis para você. Hora de levar suas habilidades para o próximo nível.

## Flash Loans ([fonte](https://finematics.com/flash-loans-explained/))

![](https://i.imgur.com/Khhg1YW.png)

Um flash loan é um recurso que permite que você pegue emprestado qualquer quantia disponível de ativos de um pool de contratos inteligentes designado, sem a necessidade de garantias. Flash loans são blocos de construção úteis na DeFi, pois podem ser usados para arbitragem, troca de garantias e autoliquidação.

Os flash loans, embora inicialmente introduzidos pelo protocolo Marble, foram popularizados pela [Aave](https://aave.com/) e [dYdX](https://dydx.exchange/).

A parte mais importante da execução de um flash loan é encontrar um provedor de flash loan. Projetos como Aave ou dYdX desenvolveram contratos inteligentes que permitem que os usuários DeFi emprestem diferentes moedas de um pool designado sob a condição de que sejam reembolsados dentro da mesma transação Ethereum. Geralmente, há um custo fixo associado ao uso de flash loans.

Uma vez que a quantia é emprestada do pool de empréstimos, ela pode ser usada para qualquer outra ação arbitrária, desde que no final da cadeia de etapas diferentes, o flash loan inicial seja reembolsado.

Existem 3 casos de uso mais comuns para flash loans: arbitragem, troca de garantias e autoliquidação.

Flash loans, assim como criptomoedas, podem ser usados para o bem e para o mal. No que diz respeito ao último, os flash loans foram usados nos ataques mais recentes à DeFi e permitiram que os hackers ampliassem seus lucros potenciais, pois não exigem nenhum fundo inicial.

Embora os flash loans sejam predominantemente usados por desenvolvedores, também é possível usá-los sem precisar codificar. Projetos como [Collateralswap](https://collateralswap.com/), [Defisaver](https://defisaver.com/) ou [Furucombo](https://furucombo.app/) tornam isso possível.

## Ataques Vampiros: Caso do Sushi ([fonte](https://finematics.com/vampire-attack-sushiswap-explained/))

<img src="https://i.imgur.com/jtxhXLi.png" width="200"/>

Usado pelo [SushiSwap](https://www.sushi.com/) para atrair mais de $1 bilhão de liquidez em menos de uma semana, um ataque vampiro é uma forma de incentivar os provedores de liquidez de uma plataforma a mover sua liquidez para outra plataforma. Isso é feito oferecendo altas recompensas por apostar tokens LP na nova plataforma e migrando os tokens apostados para a nova plataforma.

Os ataques vampiros são uma ferramenta muito poderosa para lançar um novo projeto, especialmente um novo projeto DeFi. Eles criam fortes incentivos para que os provedores de liquidez movam sua liquidez para uma nova plataforma. O conceito é muito simples, mas muito eficaz.

O problema dos ataques vampiros é que eles são muito agressivos e criam muita FOMO, o que pode levar rapidamente à perda de confiança na comunidade.

## Ampleforth ([fonte](https://finematics.com/ampleforth-explained/))

Ampleforth é uma criptomoeda com uma característica única - seu fornecimento é elástico e pode mudar diariamente, enquanto a propriedade das tokens AMPL nunca é diluída. Para alcançar isso, o protocolo Ampleforth usa 2 oráculos de preços e um conjunto de algoritmos que podem alterar automaticamente o fornecimento total de AMPL para buscar o equilíbrio de preço.

![](https://i.imgur.com/ROaGFaZ.png)

O Ampleforth visa diversificar as carteiras de criptomoedas, sendo menos correlacionado ao preço do Bitcoin em comparação com outras criptomoedas. No médio prazo, visa ser usado como garantia em protocolos DeFi. O objetivo de longo prazo do Ampleforth é criar uma alternativa ao dinheiro emitido por bancos centrais que seja adaptável a choques.

## NFTs na DeFi ([fonte](https://finematics.com/what-are-nfts-and-how-can-they-be-used-in-defi/))

NFTs são um tipo de token criptográfico que pode representar a propriedade de bens digitalmente escassos, como obras de arte ou colecionáveis, como itens de jogos. Eles são indivisíveis e cada unidade não é intercambiável e possui propriedades diferentes. Os NFTs são provavelmente escassos e indivisíveis.

Os NFTs podem ser implementados em qualquer blockchain que suporte programação de contratos inteligentes, mas os exemplos mais populares são os padrões [ERC-721](https://eips.ethereum.org/EIPS/eip-721) e [ERC-1155](https://eips.ethereum.org/EIPS/eip-1155) no Ethereum.

Na economia, fungibilidade é a característica de bens ou commodities em que cada unidade é intercambiável e indistinguível das outras.

![](https://i.imgur.com/iauRPTX.png)

- **Único** - cada NFT tem propriedades diferentes geralmente armazenadas nos metadados do token.
- **Provavelmente escasso** - geralmente há um número limitado de NFTs, com um exemplo extremo de ter apenas 1 cópia. O número de tokens pode ser verificado na blockchain, daí sua provabilidade.
- **Indivisível** - a maioria dos NFTs não pode ser dividida em denominações menores, então você não pode comprar ou transferir uma fração do seu NFT, mas pode criar um ativo derivado que representa um NFT fracionado.

No mundo da DeFi, os NFTs podem ser usados como garantia para empréstimos. No entanto, isso não é sem desafios, pois os mercados para determinados NFTs podem ser muito ilíquidos, tornando difícil avaliar com precisão a garantia.

## Escalonamento de Camada 2 ([fonte](https://finematics.com/ethereum-layer-2-scaling-explained/))

<img src="https://i.imgur.com/uKGFGIb.png" width="400"/>

A Camada 2 é um conceito amplo e podemos esperar muitos novos projetos surgindo em breve. Conforme a adoção das soluções da Camada 2 cresce, podemos esperar ver muitos mais novos aplicativos sendo construídos no Ethereum. Um dos principais motivos para isso é o aumento da composabilidade que as soluções da Camada 2 proporcionam.

Com a escalabilidade aumentada, podemos esperar que as taxas de gás diminuam. Isso é importante, pois permitirá que o Ethereum seja usado por um público mais amplo, não apenas pelos membros mais ricos da comunidade.

Existem diferentes tipos de soluções de camada 2:

- **Canais** permitem que os participantes troquem suas transações off-chain várias vezes, enviando apenas duas transações para a camada base.
- **Plasma** é uma solução de escalonamento da Camada 2 proposta originalmente por Joseph Poon e Vitalik Buterin. Ele permite aplicativos descentralizados off-chain.
- **Sidechains** são blockchains independentes compatíveis com Ethereum, com seus próprios modelos de consenso e parâmetros de bloco.
- **Rollups** fornecem escalabilidade agrupando ou "enrolando" transações de sidechain em uma única transação e gerando uma prova criptográfica, também conhecida como SNARK (argumento sucinto não interativo do conhecimento). Apenas essa prova é enviada para a camada base.

| Solução | Interoperável com Ethereum | Pode ser usada para contratos inteligentes de propósito geral? | Participação aberta* |
| :--- | :--- | :--- | :--- |
| **Canais** | Sim | Não | Não |
| **Plasma** | Sim | Não | Sim |
| **Sidechains** | Sim | Sim | Sim |
| **Rollups** | Sim | Sim | Sim |

**Participação aberta significa que qualquer pessoa pode ingressar e usar a rede sem precisar ser conhecida antecipadamente pelos outros participantes.*

## Curve ([fonte](https://resources.curve.fi/))

<img src="https://i.imgur.com/19lxrJN.png" width="400"/><br/>

[Curve Finance](https://curve.fi/) é uma exchange descentralizada para negociação de criptomoedas que se concentra na negociação eficiente de stablecoins. O foco do Curve nas stablecoins permite que os investidores evitem ativos cripto mais voláteis.

É um formador de mercado automatizado (AMM, automated market maker) que mantém taxas e deslizamentos baixos por meio do uso de [pools de liquidez](#Pools-de-Liquidez-fonte).

Assim como o [Uniswap](#Uniswap-Exchanges-Descentralizadas-fonte), os tokens podem ser trocados desde que haja liquidez. A principal diferença entre o Curve e outras DEXes é que o Curve se concentra principalmente em ativos estáveis. O Curve oferece muitas stablecoins, incluindo DAI, USDT, USDC, BUSD e TUSD.

O protocolo Curve Finance também contém o token Curve conhecido como CRV. Ele é usado principalmente para incentivar os provedores de liquidez em sua plataforma e para envolver o máximo possível de usuários na governança do protocolo.

A quantidade de liquidez que o Curve fornece permite que outras aplicações DeFi usem as pools do Curve como parte de seu ecossistema. Aplicações como Yearn Finance e Compound usam o Curve como uma solução de farming em seu ecossistema.

Uma vantagem de usar o Curve é que ele minimiza o deslizamento. O deslizamento refere-se à diferença no preço de um ativo entre o momento em que você envia a transação e o momento em que a transação é validada na blockchain.

Atualmente, o Curve possui cerca de $6 bilhões de liquidez em seus contratos.

## Convex ([source](https://docs.convexfinance.com/convexfinance/))

<img src="https://i.imgur.com/L52LD2p.png" width="400"/><br/>

Convex Finance é uma plataforma que permite aos usuários otimizar sua liquidez na Curve Finance e ganhar recompensas aumentadas na forma de tokens CRV.

A Curve utiliza um mecanismo de governança que gira em torno do veCRV: uma versão bloqueada do CRV, e para maximizar os rendimentos, os usuários devem bloquear seus CRV por 4 anos. Mas muitos desejam sair antes e, portanto, a solução da Convex foi a seguinte: todos depositam seus CRV na Convex, que aplica tudo junto, maximizando os rendimentos e os boosts existentes no protocolo Curve, e em troca, os usuários recebem cvxCRV, que é como uma versão negociável do veCRV.

Atualmente, a Convex possui cerca de $4 bilhões de liquidez em seus contratos.

# O Fim?

Incrível! Se você conseguiu completar todos os níveis - parabéns! Agora você é um Mestre em DeFi. No entanto, não há muito tempo para comemorar. As finanças descentralizadas avançam rapidamente e sempre há coisas novas para aprender.

Para se manter atualizado e aprender ainda mais sobre finanças descentralizadas, certifique-se de se inscrever no canal [Youtube (Finematics)](https://www.youtube.com/c/finematics) e seguir no [Twitter @finematics.eth](https://twitter.com/finematics).

E também me siga no [Twitter @MarcoWorms](https://twitter.com/MarcoWorms), pois estou sempre explorando e escrevendo sobre DeFi, e com mais frequência sobre o protocolo Yearn no [Yearn Blog](https://medium.com/iearn) e [Yearn Docs](https://docs.yearn.finance/).

## Recursos

Abaixo estão glossários e outros recursos para ajudá-lo a navegar:

- [glossário DeFi do yearn](https://docs.yearn.finance/resources/defi-glossary)
- [descrições de estratégias DeFi do yearn](https://docs.yearn.finance/getting-started/guides/how-to-understand-strategies-descriptions)
- [conhecimento coletivo web3 do pentacle.xyz](http://pentacle.xyz/)
- [wiki defillama](https://wiki.defillama.com/wiki/Main_Page)
- [roteiro do desenvolvedor DeFi](https://github.com/OffcierCia/DeFi-Developer-Road-Map)
- [noções básicas de segurança DeFi](https://mirror.xyz/blorms.eth/LI0i-2v2Qs5UX2NV_L6zA8JMOteoOw0jWSm4e8ZR2oo)
- [como estudar DeFi](https://0xth.notion.site/DeFi-Studies-c16a5b6fba254c719fed633bc6b3b990#45356bb2587844588c678b98644cbf8f)

## Linha do Tempo DeFi

Uma breve linha do tempo do DeFi extraída deste artigo:

- **2009:** Bloco de gênese do Bitcoin minerado.
- **2014:** Whitepaper do Ethereum publicado por Vitalik Buterin.
- **2015:** MakerDAO é lançado na testnet do Ethereum com o eDollar (mais tarde renomeado para SAI e finalmente DAI).
- **2017:** Lançamento da mainnet do Chainlink.
- **2018:** Lançamento da mainnet do Uniswap; Bancor arrecada $150 milhões em ICO.
- **2019:** Lançamento da mainnet do Compound com airdrop do token COMP em 2020; yearn.finance é lançado como o painel pessoal de yield farming de Andre Cronje.
- **2020:** Sushiswap faz fork do Uniswap e absorve mais de $1 bilhão em liquidez; Curve é lançado com o modelo de governança do CRV votado em escrow para direcionar as recompensas de mineração de liquidez de stablecoins para as ancoragens mais fortes; O verão DeFi impulsionado por incentivos COMP resulta em influxo de novos usuários e TVL atingindo quase $15 bilhões até setembro de 2020, apesar da pandemia.
- **2021:** A alta do mercado impulsiona a descentralização das exchanges (DEX) do Ethereum para o BSC, com o pancakeswap liderando o grupo; O atraso do ETH 2.0 estimula a migração para alt-L1 chains como Avalanche, Cosmos e Solana; Tokenômica votada em escrow (veTokens) se populariza com Curve e Frax; Uniswap lança o airdrop do token de governança UNI para incentivar a migração para longe do Sushiswap.
- **2022:** A liquidez entre cadeias e a interoperabilidade se tornam mais importantes do que nunca, com o ETH 2.0 não resolvendo os problemas de congestionamento a curto prazo.
