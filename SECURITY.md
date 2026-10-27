# Segurança

## Versões com suporte

Só a [versão mais recente](https://github.com/lux-insider/biohazard4-save-editor/releases/latest)
recebe correções.

## Como relatar uma falha de segurança

**Não abra uma issue pública.** Use a aba
[**Security → Report a vulnerability**](https://github.com/lux-insider/biohazard4-save-editor/security/advisories/new)
do repositório: o relato fica privado até a correção sair.

Conte o que acontece, como repetir e, se possível, um arquivo de exemplo
(sem dados pessoais). A resposta vem em até 7 dias.

## O que o programa faz com os seus dados

- Não acessa a internet.
- Lê e grava só o save que você abrir. Antes de gravar, guarda uma cópia na
  pasta `backups`.
- O `kv.bin` (opcional) fica só na pasta `console` do programa e serve apenas
  para assinar o save com a chave do seu console. Ele nunca é copiado para
  outro lugar.
