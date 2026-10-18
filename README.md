# cofrim.github.io

Raiz de https://cofrim.github.io/: a página inicial do app Cofrim (a da tela de consentimento do Google, Google Auth
Platform › Branding), com os links da política de privacidade e da exclusão de dados (no repositório `cofrim-web`), e o
arquivo de verificação do Google Search Console (`google*.html`, não apagar), que prova ao Google que o endereço é nosso.

Convite da conta compartilhada (app da Google Play, repositório `cofrim-playstore`):

- `convite/index.html`: o link `https://cofrim.github.io/convite/?c=<código>` que o app gera em "Convidar". Com o app
  instalado, o Android abre o app direto (App Links) e a página nem aparece; sem o app, ela leva à Google Play com o
  código no referrer da instalação, e o app abre o convite sozinho na primeira abertura.
- `.well-known/assetlinks.json`: prova ao Android que o endereço é do app `br.cofrim.app` (App Links). Leva a impressão
  SHA-256 da chave de assinatura da Google Play (Play Console › Testar e lançar › Configuração › Integridade do app ›
  Assinatura de apps), no lugar de `COLE_AQUI_A_SHA256_DA_CHAVE_DE_ASSINATURA_DA_PLAY`.
- `.nojekyll`: sem ele o GitHub Pages não publica pastas que começam com ponto (`.well-known`).
