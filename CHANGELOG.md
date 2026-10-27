# Histórico de versões

Todas as mudanças relevantes do BIOHAZARD 4 SAVE EDITOR, da mais nova para a
mais antiga. As versões seguem o [Versionamento Semântico](https://semver.org/lang/pt-BR/).

---

## 1.0.0 — 2026-10-25

Primeira versão.

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
  primeiro espaço livre da maleta (deitado ou de pé), inclusive as maletas P,
  M, G e GG.
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
