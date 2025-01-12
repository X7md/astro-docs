---
title: Faça Deploy do seu Site Astro com Buddy
description: Como fazer o deploy do seu site Astro para web usando Buddy.
layout: ~/layouts/DeployGuideLayout.astro
i18nReady: true
---

Você pode fazer o deploy do seu projeto Astro usando [Buddy](https://buddy.works/), uma solução de continuous deployment que pode fazer o build e push do seu site para muitos diferentes alvos de deploy, incluindo servidores FTP (em Inglês, "File Transfer Protocol") e provedores de hospedagem em nuvem.

:::note
O Buddy não irá hospedar o seu site. Em vez disso, ele o ajuda a gerenciar o processo de build e a entregar o resultado a uma plataforma de deploy de sua escolha.
:::

## Como fazer o Deploy

1. Crie uma conta no **Buddy** [aqui](https://buddy.works/sign-up).
2. Crie um novo projeto e conecte-o com um repositório git (GitHub, GitLab, BitBucket, qualquer repositório Git privado ou você pode usar o Buddy Git Hosting).
3. Adicione um novo pipeline.
4. Nesse novo pipeline adicione um **[Node.js](https://buddy.works/actions/node-js)** action.
5. Nesse action adicione:

   ```bash
   npm install
   npm run build
   ```

6. Adicione um deployment action — há muitos para escolher, você pode navegar por eles [aqui](https://buddy.works/actions). Embora suas configurações possam ser diferentes, lembre-se de definir o **Source path** para `dist`.
7. Clique no botão **Run**.
