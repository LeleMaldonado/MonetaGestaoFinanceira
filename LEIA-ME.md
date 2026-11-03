# Moneta — app de controle financeiro (instalável no celular)

Esta pasta é o app Moneta pronto para ser publicado de graça no **GitHub Pages** e instalado
no celular como app (PWA), sem precisar compilar nada.

## 1. Publicar no GitHub Pages

1. Crie uma conta em github.com (se ainda não tiver) e clique em **New repository**.
2. Dê um nome, por exemplo `moneta`, deixe **Public** e crie o repositório.
3. Clique em **Add file → Upload files** e envie **todos os arquivos desta pasta**
   (`index.html`, `manifest.webmanifest`, `sw.js`, os três `icon-*.png` e `.nojekyll`).
   Confirme em **Commit changes**.
4. Vá em **Settings → Pages**. Em **Build and deployment**, escolha
   **Deploy from a branch**, branch `main` e pasta `/ (root)`. Salve.
5. Espere cerca de 1 a 2 minutos. O endereço aparece na mesma tela e tem o formato
   `https://SEU-USUARIO.github.io/moneta/`.

## 2. Instalar no celular

- **iPhone:** abra o endereço no **Safari** → botão Compartilhar → **Adicionar à Tela de Início**.
- **Android:** abra o endereço no **Chrome** → menu (três pontos) → **Instalar app** ou
  **Adicionar à tela inicial**.

O app abre em tela cheia, com o ícone do Moneta, e funciona sem internet (as cotações
automáticas precisam de internet).

## 3. Cotações automáticas

- **Criptomoedas:** são buscadas automaticamente na CoinGecko, sem cadastro e sem token, em reais.
  Use o código da moeda (BTC, ETH, SOL...) no campo "Moeda".
- **Ações e FIIs:** usam a brapi, que precisa de um token grátis.
  1. Crie uma conta em **brapi.dev** e copie o **token** do painel.
  2. No app, abra a aba **Investimentos**, vá até o fim da página, abra **Cotações automáticas (brapi)**,
     cole o token e toque em **Salvar**.
- As cotações são buscadas ao abrir o app e a cada 30 minutos com o app aberto. O botão de atualizar,
  no card Posição, força uma nova busca.

Plano gratuito da brapi: 15.000 consultas por mês, 1 ativo por consulta e dados atualizados a cada
30 minutos. O app respeita esse intervalo para não gastar a cota à toa.

**O que fica de fora:** ativos do **exterior** (como VOO) não existem na brapi. Para esses, digite a
cotação em reais na linha do ativo, na Posição. Renda fixa e caixa seguem pelo valor aplicado.

## 4. Seus dados

- Ficam **só no aparelho** (armazenamento do navegador). Celular e computador não sincronizam.
- Use **Resumo → Backup dos dados → Exportar** para guardar uma cópia e **Importar** para restaurar.
- **Apagar todos os dados** (no mesmo card) deixa o app vazio para começar do zero.
- O token da brapi fica salvo só no aparelho e não entra no backup.

## 5. Atualizar o app

Quando houver uma versão nova, substitua os arquivos no repositório (Add file → Upload files,
sobrescrevendo). O app abre sempre a versão mais nova quando há internet; se o celular
guardar a versão antiga, feche e abra o app de novo.
