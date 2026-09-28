# Xbox Series S Robot White para GamePad Viewer

O pacote usa a fotografia frontal oficial do **Xbox Wireless Controller Robot White** e inclui o direcional híbrido e o botão Share do controle Series X|S. A referência visual foi [a página oficial da Microsoft](https://www.microsoft.com/en-us/p/xbox-wireless-controller--robot-white--robot-white/8XN59CRBSQGZ/JBFJ).

O pacote contém **46 SVGs**. A base e os botões comuns usam **650 × 463 px**. Os sticks e gatilhos da pasta `pecas-individuais` têm as dimensões próprias exigidas pelos campos do editor.

O arquivo `fonte/foto-recortada-original.png` é a imagem transparente enviada pelo usuário, preservada em resolução de 2000 × 2000 px. As imagens da pasta `previas` mostram a base e alguns estados dos botões para conferir a aparência antes de configurar o editor. A raiz do pacote contém apenas os SVGs e estas instruções.

O SVG da base inclui a foto e sua transparência em arquivos compactados internamente. Isso reduz o tamanho do SVG para facilitar a visualização e o uso do link **Raw** no GitHub.

## Sticks e gatilhos individuais

A pasta `pecas-individuais` contém oito SVGs: estado neutro e pressionado de cada stick (`stick-esquerdo`, `stick-direito`) e gatilho (`gatilho-esquerdo`, `gatilho-direito`). Eles foram desenhados para a foto deste controle, tomando como referência as peças do Xbox no GamePad Viewer. **Os dois arquivos de cada stick medem exatamente 83 × 83 px**, inclusive o `viewBox`; nenhum brilho ou deslocamento ultrapassa essa área. Os gatilhos visíveis nesta foto têm **138 × 48 px**. Use o arquivo `*-neutro.svg` no campo **Neutral State Image URL** e `*-pressionado.svg` em **Pressed State Image URL**.

| Peça | Width | Height | Left Position | Top Position |
| --- | ---: | ---: | ---: | ---: |
| Stick esquerdo | 83 | 83 | 122 | 91 |
| Stick direito | 83 | 83 | 369 | 191 |
| Gatilho esquerdo (LT) | 138 | 48 | 98 | 4 |
| Gatilho direito (RT) | 138 | 48 | 414 | 4 |

As imagens `previas/previa-peca-*.png` mostram os estados pressionados colocados nessas posições. A pasta `versoes-tela-inteira` guarda as alternativas LS/RS/LT/RT de **650 × 463 px**. **Não use essas versões nos campos configurados como 83 × 83 px**; nesse caso, use somente `pecas-individuais/stick-...svg`.

- `xbox-series-s-base.svg`: controle conectado.
- `xbox-series-s-desconectado.svg`: silhueta vermelha.
- `xbox-series-s-neutro-NOME.svg`: relevo discreto no estado normal.
- `xbox-series-s-pressionado-NOME.svg`: botão visualmente afundado com indicação azul transparente.

Nomes disponíveis na pasta principal: `A`, `B`, `X`, `Y`, `DU`, `DD`, `DL`, `DR`, `LB`, `RB`, `VIEW`, `MENU`, `SHARE` e `GUIDE`. LS, RS, LT e RT ficam em `pecas-individuais` e `versoes-tela-inteira`.

No editor, configure a base com **Width = 650** e **Height = 463**. Para os botões comuns da pasta principal, use a mesma largura e altura com **Top = 0** e **Left = 0**, colocando cada SVG neutro e pressionado nos campos correspondentes. Para sticks e gatilhos, use a tabela acima. Os arquivos precisam de URLs HTTPS diretas antes de preencher os campos do editor.

As entradas físicas dependem do modo em que o controle aparece no navegador. Use o teste de gamepad para confirmar VIEW, MENU, SHARE, GUIDE e as entradas dos gatilhos.

## Correspondência com o preset Xbox One do editor

| Peça do editor | SVG `NOME` |
| --- | --- |
| A/Cross, B/Circle, X/Square, Y/Triangle | A, B, X, Y |
| Left/Right Thumbstick | `pecas-individuais/stick-esquerdo` e `stick-direito` |
| Left/Right Bumper | LB, RB |
| Left/Right Trigger | `pecas-individuais/gatilho-esquerdo` e `gatilho-direito` |
| Select, Start, PS/Guide | VIEW, MENU, GUIDE |
| D-Pad Up/Down/Left/Right | DU, DD, DL, DR |

O botão **SHARE** é adicional no Series X|S. O suporte para sua entrada depende do navegador e da forma de conexão; não associe a outra peça sem testá-lo no controle físico.
