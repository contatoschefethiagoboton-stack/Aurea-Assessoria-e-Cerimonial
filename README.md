# Áurea Assessoria de Eventos — site

Site institucional estático (HTML5 + Tailwind CSS via CDN). Não precisa de build nem de servidor.

## Estrutura
```
index.html            página completa
assets/logo-aurea.png logo com fundo transparente
assets/favicon.svg    ícone da aba do navegador
render.yaml           configuração para o Render
robots.txt            libera o site para o Google
sitemap.xml           mapa do site para o Google
```

## Antes de publicar
Os contatos já estão configurados no bloco `CONFIG` perto do fim do `index.html` (WhatsApp (19) 99192-6181, Instagram @aureaassessoria.cps, e-mail aureaassessoria@gmail.com). Para alterar, edite:
- `whatsapp`: 55 + DDD + número, só dígitos (ex.: 5519999999999)
- `instagram`: link do perfil
- `email`: e-mail de contato

O domínio `aureaassessoria.com.br` já está configurado no `index.html` (canonical e tags de compartilhamento), no `robots.txt` e no `sitemap.xml`.

## Publicar no GitHub
1. Crie um repositório novo em github.com (ex.: `aurea-site`).
2. Clique em **Add file → Upload files**, arraste todo o conteúdo desta pasta (incluindo a pasta `assets`) e clique em **Commit changes**.

## Publicar no Render
1. Em dashboard.render.com, clique em **New → Static Site** e conecte o repositório.
2. Build Command: deixe em branco. Publish Directory: `.`
3. Clique em **Create Static Site**. A cada alteração enviada ao GitHub, o Render publica de novo sozinho.

(Alternativa: **New → Blueprint** usa o `render.yaml` automaticamente.)

## Domínio próprio (aureaassessoria.com.br)
1. No Render, abra o site → **Settings → Custom Domains → Add Custom Domain** e digite `aureaassessoria.com.br`. O Render adiciona também o `www.aureaassessoria.com.br` e redireciona o www para o domínio principal.
2. No Registro.br, abra o domínio → **DNS → Editar zona** (se aparecer "Configurar endereçamento", escolha usar os servidores DNS do Registro.br) e crie:
   - Tipo **A**, nome em branco (`@`), valor: o IP que o Render mostrar para o domínio principal.
   - Tipo **CNAME**, nome `www`, valor: o endereço `.onrender.com` do seu site (o Render mostra qual).
3. Volte ao Render e clique em **Verify**. A propagação pode levar de minutos a algumas horas; o certificado HTTPS (cadeado) é emitido automaticamente.
