# Hlustaðu

Einföld „Væntanlegt“ síða fyrir hlustadu.is. Engar pakkauppsetningar eða byggingarskref eru nauðsynleg.

## Skoða síðuna í þróun

Keyrðu `python3 -m http.server 8000` úr möppu safnsins og opnaðu síðuna í vafra á tölvunni sem keyrir þjóninn.

## Birta á GitHub Pages

1. Settu þessar skrár á `main` í GitHub-safninu `asgeirpall-pixel/Hlustadu-heimasida`.
2. Opnaðu **Settings → Pages**. Undir **Build and deployment** velurðu **Deploy from a branch**, síðan `main` og `/ (root)`, og vistar.
3. Undir **Custom domain** skráirðu `hlustadu.is`. Skráin `CNAME` geymir einnig þetta lén.
4. Áður en DNS er tengt er mælt með að staðfesta eignarhald á léninu í **Settings → Pages** á GitHub-notandaaðganginum. GitHub gefur upp TXT-færslu fyrir staðfestinguna.
5. Stilltu DNS hjá DNS-þjónustuaðila lénsins samkvæmt töflunni hér að neðan. ISNIC skráir lénið; ef DNS-færslur eru ekki aðgengilegar þar þarf DNS-hýsingu og að skrá nafnaþjóna hennar hjá ISNIC.
6. Þegar GitHub hefur staðfest DNS og gefið út vottorð skaltu virkja **Enforce HTTPS** í Pages-stillingunum. DNS-breytingar geta tekið allt að sólarhring að dreifast.

| Tegund | Nafn | Gildi |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | asgeirpall-pixel.github.io |

`@` táknar sjálft lénið `hlustadu.is`; sum kerfi nota autt heiti eða fullt lénið í staðinn. Varðveittu póstfærslur (MX og tengdar TXT-færslur) ef þær eru til. Fjarlægðu eldri A/AAAA-færslur fyrir sama vefheiti sem vísa á aðra hýsingu. Ekki setja algilda wildcard-færslu fyrir GitHub Pages.

GitHub Pages er í boði fyrir opinber söfn á GitHub Free; einkasöfn þurfa áskrift sem styður Pages.

Opinberar leiðbeiningar: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
