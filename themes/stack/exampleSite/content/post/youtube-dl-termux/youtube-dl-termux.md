---
title: Youtube-dl no termux
date: 2021-06-23 17:29:00
categories:
- Termux
- Youtube-dl
---
Youtube-dl é um gerenciador de downloads de código livre de conteúdo audovisual no Youtube e outros sites de vídeos. Em Outubro de 2020,  youtube-dl era um dos projetos com mais "estrelas" no Github, com mais de 72 mil estrelas. 
Fontes: [XDA](https://forum.xda-developers.com/t/install-youtube-dl-in-termux.4061221/) | [GIT](https://github.com/shukryshuk/androidydl) | [WIKI](https://www.google.com/url?sa=t&source=web&rct=j&url=https://pt.m.wikipedia.org/wiki/Youtube-dl&ved=2ahUKEwjBo9v-4ZbvAhVCk1kKHRGyBQ0QmhMwBXoECAcQAg&usg=AOvVaw1Yfx2W_ej3OQyxmcAQRRtZ)

### Atenção:
- Legalmente o download de qualquer tipo de conteudo sem autorização ou consentimento dos autores é considerado crime;
- Não me responsabilizo por qualquer tipo de dano ou por não funcionar como deveria. Youtube-dl é de código aberto e qualquer coisa que você faça, é de sua responsabilidade. 

### Instalação:
`termux-setup-storage ; curl -s -L http://bit.ly/38m5iNB | bash`

Permita o acesso a memória interna e espere ~1m para concluir a instalação. Todo arquivo que você baixar, vai ir para `/storage/emulated/0/Youtube`.

- Para atualizar: `pip install youtube-dl -U`

#### Como usar depois de instalar? 
- Qualquer tipo de dúvida, leia a ajuda: ´youtube-dl --help´

#### Versão simples de uso:
Vá no vídeo que você quer baixar e clique em compartilhar. Selecione o app termux e espere o download acabar. 

#### Alternativa simples:
1. Copie o link do vídeo que você quer baixar;
2. Abra o termux e escreva: ´youtube-dl [link]´

#### Download com escolha de qualidade:
`youtube-dl -F [link]`

Escolha o número que corresponde com a qualidade desejada e de o comando:

`youtube-dl -f [número] [site]`

#### Por exemplo:
`youtube-dl -f 22 https://youtu.be/H1FbySVjmYY`

#### Extrair áudio do vídeo:
`youtube-dl -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0 [link]`