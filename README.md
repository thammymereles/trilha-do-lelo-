# Trilha do Lelo

App gratuito para crianças aprenderem a ler brincando, pensado para quem **ainda não sabe ler**: todas as telas são narradas pelo Lelo, uma tartaruga, e a criança joga só tocando e ouvindo.

Funciona no navegador do celular, do tablet ou do computador. Não precisa instalar nada nem criar conta.

## O que tem no app

A trilha tem 6 etapas e 174 brincadeiras:

| Etapa | O que a criança faz |
|---|---|
| Descobrindo as Letras | Ouve o nome da letra e acha a letra certa, descobre o que começa com cada letra, liga a letra grande à pequena |
| Desenhando as Letras | Passa o dedo em cima da letra pontilhada (maiúscula e minúscula) |
| O Som das Letras | Ouve uma palavra e escolhe a letra do primeiro som |
| Juntando os Sons | Ouve e toca na sílaba certa, monta palavras com sílabas |
| Começando a Ler | Acha a palavra certa, lê a palavra e acha a figura, lê frases curtas |
| Pensar e Mexer | Lógica: o que vem depois na fila, qual figura é diferente, do menor ao maior, jogo da memória. Coordenação motora: passar o dedo em caminhos (reta, onda, zigue-zague), arrastar figuras até a sombra, estourar bolhas. Mexa o corpo: pausas longe da tela (pular, equilibrar, fazer letras com o corpo, bater palmas nas sílabas). Carros e trens: dirigir o carro até a garagem certa, corrida pegando estrelas e letras, trem das sílabas |

Os jogos de Pensar e Mexer entram na trilha recomendada um a cada 2 letras, para variar o ritmo.

Feito para quem ainda não lê:

- Toda tela fala. O botão amarelo 🔊 repete a instrução quando a criança quiser.
- Cada figura tem o próprio botão 🔊 para ouvir o nome antes de responder.
- O erro explica o que aconteceu ("Essa é a letra tê. Procure a letra bê."). Depois de 2 erros, a resposta certa brilha.
- Nas frases, o Lelo lê junto e cada palavra acende enquanto ele fala.
- As respostas ficam na parte de baixo da tela, perto do polegar.
- Para sair de um jogo, é preciso segurar o botão da casinha por 1 segundo, o que evita saídas sem querer.
- Há uma única recomendação de "próxima brincadeira", a mesma em todo o app.
- Todas as figuras são ilustrações 3D, iguais em qualquer celular ou computador.
- Os exemplos se alternam: cada vez que a criança abre uma letra, aparece outra palavra (A de abelha, A de amor, A de árvore, A de amigo...). Cada letra tem de 2 a 6 palavras.

Área dos pais, protegida por uma conta de multiplicação:

- várias crianças no mesmo aparelho;
- tempo de uso por dia;
- letras com mais erros;
- últimas brincadeiras;
- escolha da voz e da velocidade da fala.

## Como publicar no GitHub Pages (grátis)

1. Crie uma conta em [github.com](https://github.com), se ainda não tiver.
2. Clique em **New repository** (ou no **+** no alto da página).
   - **Repository name:** `trilha-do-lelo`
   - Marque **Public**.
   - Clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file** (ou **Add file › Upload files**).
4. Arraste os arquivos `index.html` e `README.md` desta pasta e clique em **Commit changes**.
5. Vá em **Settings › Pages**.
   - Em **Source**, escolha **Deploy from a branch**.
   - Em **Branch**, escolha **main** e a pasta **/ (root)**. Clique em **Save**.
6. Espere 1 ou 2 minutos e atualize a página. O endereço aparece no alto, por exemplo:
   `https://SEU-USUARIO.github.io/trilha-do-lelo/`

Esse é o link para divulgar. Para atualizar o app depois, envie um `index.html` novo da mesma forma (passo 4); o site se atualiza sozinho.

## Como testar no seu computador

Abra o arquivo `index.html` com o Chrome, o Edge ou o Safari. Na primeira vez, toque em qualquer lugar da tela para a voz começar: os navegadores só liberam o som depois de um toque.

## Onde fica o progresso

Nesta versão, o progresso fica salvo **no próprio aparelho**, dentro do navegador. Não passa para outros aparelhos, e limpar os dados do navegador apaga tudo. Nada do que a criança faz é enviado para a internet.

O app usa as fontes Andika e Fredoka do Google Fonts, então o navegador baixa as fontes do Google ao abrir a página.

As figuras 3D são as [Fluent Emoji](https://github.com/microsoft/fluentui-emoji) da Microsoft (licença MIT), baixadas do jsDelivr na primeira vez que aparecem. Se o aparelho estiver sem internet, aparece no lugar o emoji do próprio aparelho.

## Voz

A narração usa a voz que já vem no aparelho (síntese de voz do navegador):

- **Android:** se o app ficar mudo, vá em Configurações › Sistema › Idioma › Saída de texto para fala e instale **Português (Brasil)**.
- **iPhone e iPad:** Ajustes › Acessibilidade › Conteúdo Falado › Vozes › **Português (Brasil)**.

A Área dos pais avisa quando o aparelho não tem voz em português. A qualidade da voz muda de aparelho para aparelho. Os sons isolados das letras (como /mmm/) não saem perfeitos com voz sintética; uma voz humana gravada resolveria isso.

## Como mudar o conteúdo

Está tudo num arquivo só, o `index.html`. O conteúdo fica no começo do `<script>`:

- `LETTERS`: o nome falado de cada letra e as palavras com figura (emoji) de cada uma. Os exemplos se revezam na ordem da lista.
- `ABSTRATO`: palavras que não aparecem como figura "errada" nos jogos, porque a figura pode ter outro nome (o coração de "amor" também é "coração").
- `FAM`: as famílias de sílabas e as palavras para montar (`'BO-LA'`, figura, palavra falada).
- `LER`: as palavras e frases da etapa "Começando a Ler".
- `ORDER`: a ordem em que a trilha recomenda as letras.
- `CATS`, `SEQ_POOL`, `SHADOW_POOL` e `PATHS`: as figuras dos jogos de Pensar e Mexer (grupos do "qual é diferente", figuras das filas e das sombras, e os caminhos).
- `GARAGE_PICS`, `BODY` e `BODY_LETTERS`: os bichos das garagens e os movimentos do "Mexa o corpo".

Para trocar uma figura, troque o emoji: o app mostra a versão 3D dele sozinho. Para trocar uma palavra, troque o texto. O resto do app se ajusta sozinho.
