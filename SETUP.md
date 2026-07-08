# Como colocar o site no ar (fazer uma vez só)

Isso aqui é só pra você configurar. Depois disso pronto, sua esposa só usa o link `/admin` pra editar — nunca mais precisa mexer em código ou nesse guia.

## 1. Subir o código pro GitHub
1. Crie um repositório novo no GitHub (pode ser privado).
2. Suba todos os arquivos desta pasta pra esse repositório (via GitHub Desktop, ou `git init` / `git add` / `git commit` / `git push` pelo terminal).

## 2. Criar o site no Netlify
1. Crie uma conta em https://app.netlify.com (dá pra entrar direto com a conta do GitHub).
2. Clique em **"Add new site" → "Import an existing project"**.
3. Escolha **GitHub** e selecione o repositório que você acabou de criar.
4. Nas configurações de build, deixe **Build command** vazio e **Publish directory** como `.` (o `netlify.toml` já vem configurado assim). Clique em **Deploy**.
5. Em alguns segundos o site estará no ar num endereço tipo `https://nome-aleatorio.netlify.app`. Se quiser, troque esse nome em **Site settings → Change site name**.

## 3. Ativar o login do painel (Identity)
1. No painel do Netlify, vá em **Site settings → Identity → Enable Identity**.
2. Ainda em Identity, procure **Registration** e deixe como **Invite only** (assim só quem você convidar consegue logar).
3. Em **Services**, ative o **Git Gateway** (botão "Enable Git Gateway"). É isso que permite o painel salvar as edições direto no GitHub sem sua esposa precisar de conta lá.

## 4. Convidar sua esposa
1. Ainda em **Identity**, clique em **Invite users** e coloque o e-mail dela.
2. Ela vai receber um e-mail do Netlify pra definir uma senha.
3. Depois de definir a senha, ela já pode acessar `https://SEUSITE.netlify.app/admin` pra editar.

## Como ela edita
1. Abrir `https://SEUSITE.netlify.app/admin` e fazer login com e-mail/senha.
2. Clicar em **"Vitrine e WhatsApp"**.
3. Trocar foto (clicando no campo Foto), preço, nome ou descrição de qualquer produto — ou adicionar/remover produtos na lista.
4. Clicar em **"Publish"** no canto superior. Em cerca de 1 minuto o site já atualiza pra todo mundo.

## Observações
- Fotos enviadas pelo painel ficam salvas na pasta `images/uploads` do repositório automaticamente.
- Toda edição vira um commit no GitHub — dá pra ver o histórico de mudanças por lá se precisar reverter algo.
