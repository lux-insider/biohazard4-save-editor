# Histórico de versões

Todas as mudanças relevantes do BIOHAZARD 4 SAVE EDITOR, da mais nova para a
mais antiga. As versões seguem o [Versionamento Semântico](https://semver.org/lang/pt-BR/).

---

## 1.0.0 — 2026-10-25

Primeira versão.

### Correções depois do lançamento
As correções entram na própria 1.0.0 (o download da release é atualizado).

- **29/10 — Maleta mais parecida com a do jogo:** as caixas de munição
  aparecem de frente, com o rótulo, e o Broken Butterfly e o Killer7 de lado
  (antes eram vistos de cima e viravam uma tira fina); cada item mostra no
  canto as balas no pente ou a quantidade; as casas ficaram mais escuras, as
  figuras ocupam quase todo o espaço do item e o item escolhido ganhou o
  realce claro do cursor do jogo.
- **31/10 — P.R.L. 412 na janela Adicionar item:** a arma de laser agora pode
  ser colocada na maleta (testada no console: aparece, equipa e funciona). As
  outras armas de outros modos continuam de fora, porque no jogo do Leon
  aparecem com o modelo errado ou sem munição.
- **31/10 — Save do PC (Steam):** o editor abre e grava também o
  `savegame00.sav` do Resident Evil 4 Ultimate HD Edition, com as mesmas
  telas (pesetas, vida, roupas e maleta), testado no jogo. O painel Arquivo
  mostra a versão e a conta Steam.
- **31/10 — Data dos slots:** o mês aparecia um a mais (31/11 em vez de
  31/10).
- **01/11 — Aba EXTRAS:** os 16 desbloqueios do arquivo (modos de jogo,
  personagens do Mercenaries, roupas especiais e armas especiais do Mercador),
  com a arte do jogo, e o Round do slot. Do Round 02 em diante o Mercador
  vende as armas especiais, a Matilda e o Lança-foguetes Infinito. Testado no
  jogo do PC.
- **02/11 — EXTRAS no Xbox 360:** testado no console. Todos os desbloqueios
  aparecem no jogo, igual ao PC: Separate Ways, Assignment Ada, The
  Mercenaries com os 5 personagens, Ada's Report, a Dificuldade Profissional,
  as roupas e as armas do Mercador.
- **03/11 — Botão TIRAR DA MALETA:** em janelas menores, a rolagem do painel
  do item não chegava ao fim e escondia o botão. O botão agora fica fixo no
  rodapé do painel, e a rolagem alcança todas as opções da arma.
- **03/11 — Aba ITENS:** a lista de todos os itens do slot saiu da aba Maleta
  e ganhou uma aba própria, com o editor do item ao lado. A maleta desenhada
  ficou maior.
- **03/11 — Aba HISTÓRIA:** os 39 arquivos do jogo para consulta, traduzidos
  para o português, com as artes originais: campanha do Leon, manuais e
  Separate Ways. Marca os que o slot escolhido já coletou. Os arquivos saíram
  da lista da aba Itens, mas continuam no save.
- **03/11 — Tamanho da maleta:** a aba Maleta agora escolhe a maleta do slot:
  P, M, G ou GG. Só diminui se todos os itens continuarem dentro. As maletas
  não apareciam na janela Adicionar item, ao contrário do que dizia o LEIA-ME.
- **03/11 — Aba Save sem rolagem no painel direito:** o slot escolhido e o
  arquivo aparecem inteiros, em qualquer tamanho de janela.

### Saves
- **Resident Evil 4 HD do Xbox 360:** só abre pacotes CON de save do jogo
  (Title ID `4343081C`), como `game00_en` e `game00_ge`.
- Os **20 slots** da tela de carregar, da campanha do Leon e do Separate Ways
  da Ada, com data, área, pesetas e vida.
- **Pesetas** (até 9.999.999) e **vida** atual e máxima do Leon ou da Ada
  (até 2.400), com o botão VIDA CHEIA.
- **Roupas:** Normal, Especial 1 e Especial 2, como no menu do jogo (Leon e
  Ashley juntos; a Ada tem as dela). O editor grava a roupa do modelo pela
  mesma regra que o jogo usa ao carregar.

### Maleta e itens
- **Armas:** níveis de melhoria (poder de fogo, capacidade, cadência e
  recarga), com os valores de cada nível tirados do executável. O último nível
  de capacidade das armas com melhoria exclusiva é a munição infinita. Balas
  no pente, com o botão ENCHER.
- **Quantidade** de munição, ervas, granadas e tesouros, até o máximo que o
  jogo aceita em cada espaço.
- **Adicionar item:** os 268 itens do jogo, com figura e tamanho em casas, no
  primeiro espaço livre da maleta (deitado ou de pé).
- **Tirar da maleta** qualquer item, menos a arma equipada. Acessórios
  montados na arma tirada ficam soltos, como o jogo grava.

### Visual
- Tudo vem dos arquivos do jogo: arte de fundo, logo, retratos, a maleta
  montada com as peças da tela de inventário e as imagens dos capítulos em
  cada slot.
- **Figuras dos 208 itens** desenhadas a partir dos modelos 3D do jogo, com as
  texturas originais. As misturas de ervas mostram as folhas dentro do tubo e
  as tampinhas usam as fotos do próprio jogo.
- **Figuras das roupas** desenhadas a partir dos modelos dos personagens.
- **Fonte do jogo** convertida em TrueType e embutida.
- Interface nativa em Slint, sem navegador nem WebView. Funciona a partir de
  1280×700.

### Assinatura e segurança
- O save sai sempre assinado e pronto para o console, com a chave interna do
  programa ou com o `console/kv.bin` do seu console, se existir.
- **Gravação segura:** grava numa cópia, lê de volta e confere as verificações
  de todos os slots, os hashes e a assinatura; só então troca pelo original.
  Backup automático na pasta `backups/` antes de cada gravação.
- Só os slots alterados são regravados; os outros saem idênticos.

### Validação
- **No console:** saves gravados pelo código do editor abriram num Xbox 360
  real. Canhão de Mão e Metralhadora de Gângster com a capacidade exclusiva
  ficaram com munição infinita, a maleta GG adicionada passou a valer e a
  escolha de roupa Especial 2 carregou Leon de gângster e Ashley de armadura.
- Formato conferido nos saves de exemplo: todos os CRCs batem e os 319 itens
  de maleta cabem sem se sobrepor.
