# Áurea Assessoria de Eventos — site

Site institucional estático (HTML5 + Tailwind CSS via CDN). Não precisa de build nem de servidor.

## Estrutura
```
index.html            página completa
assets/logo-aurea.png logo com fundo transparente
assets/favicon.svg    ícone da aba do navegador
render.yaml           configuração para o Render
robots.txt            libera o site para o Google
```

## Antes de publicar
Os contatos já estão configurados no bloco `CONFIG` perto do fim do `index.html` (WhatsApp (19) 99192-6181, Instagram @aureaassessoria.cps, e-mail aureaassessoria@gmail.com). Para alterar, edite:
- `whatsapp`: 55 + DDD + número, só dígitos (ex.: 5519999999999)
- `instagram`: link do perfil
- `email`: e-mail de contato

Depois que o site estiver no ar, troque `SEU-DOMINIO.onrender.com` na tag `og:image` pelo endereço real.

## Publicar no GitHub
1. Crie um repositório novo em github.com (ex.: `aurea-site`).
2. Clique em **Add file → Upload files**, arraste todo o conteúdo desta pasta (incluindo a pasta `assets`) e clique em **Commit changes**.

## Publicar no Render
1. Em dashboard.render.com, clique em **New → Static Site** e conecte o repositório.
2. Build Command: deixe em branco. Publish Directory: `.`
3. Clique em **Create Static Site**. A cada alteração enviada ao GitHub, o Render publica de novo sozinho.

(Alternativa: **New → Blueprint** usa o `render.yaml` automaticamente.)

## Domínio próprio
No Render, abra o site → **Settings → Custom Domains**, adicione o domínio e copie os registros DNS indicados para o painel onde o domínio foi registrado (ex.: Registro.br).
