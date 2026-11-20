# Super Coins — projeto Android

## Conteúdo
- `www/index.html`: jogo arcade jogável.
- `capacitor.config.json` e `package.json`: configuração da aplicação.
- `.github/workflows/android-apk.yml`: compilação automática de APK no GitHub Actions.

## Gerar o APK usando apenas Android
1. Descarrega e extrai o ZIP no telemóvel.
2. Cria uma conta gratuita em https://github.com/ e um repositório novo chamado `super-coins`.
3. No repositório, usa **Add file > Upload files** e envia os ficheiros e pastas do projeto extraído. Mantém a pasta `.github/workflows` e o ficheiro `android-apk.yml` no respetivo caminho.
4. Faz **Commit changes** para o ramo `main`.
5. Abre o separador **Actions** do repositório. Se necessário, ativa workflows.
6. Abre o workflow **Build Super Coins APK**. Aguarda que termine com marca verde.
7. Abre a execução concluída e, em **Artifacts**, descarrega `super-coins-debug-apk`.
8. Extrai o ZIP do artefacto. Dentro estará `app-debug.apk`. Toca nele para instalar. Se o Android pedir, permite instalar aplicações desta origem.

A compilação na nuvem requer internet e uma conta GitHub. O APK produzido é de depuração para testes, não é ainda a versão assinada de lançamento para Google Play.

## Google AdMob — estado
A integração AdMob ainda NÃO está incluída neste protótipo. O botão de recompensa é apenas uma demonstração. Não há anúncios reais nem receitas nesta versão.

Para integrar anúncios reais é necessário:
- Registar a app Android no AdMob e obter o App ID.
- Criar unidades de anúncios (rewarded e interstitial).
- Integrar um plugin/SDK nativo compatível com Capacitor 7.
- Configurar o App ID no `AndroidManifest.xml` e os IDs das unidades no código.
- Implementar consentimento de privacidade UMP/RGPD para utilizadores no EEE.
- Testar apenas com anúncios de teste até à publicação.

IDs de teste oficiais Google (não geram receita):
- Interstitial: `ca-app-pub-3940256099942544/1033173712`
- Rewarded: `ca-app-pub-3940256099942544/5224354917`

Nunca cliques nos teus próprios anúncios reais. Usa IDs de teste durante desenvolvimento; a Google alerta que tráfego inválido pode suspender a conta.

## Publicação
Para publicar na Google Play, será necessário preparar uma versão de lançamento assinada (AAB), política de privacidade, classificação etária, formulário de segurança dos dados, consentimento aplicável e cumprir os requisitos atuais da Play Console. A publicação pode exigir uma conta Play Console paga.
