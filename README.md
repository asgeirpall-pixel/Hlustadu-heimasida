# hlustaðu.

Forsíða fyrir hlustadu.is. Einfaldur kyrrstæður vefur með sér uppsetningu fyrir síma (760px og minna) og tölvu. Engin pakkauppsetning eða byggingarskref.

## Staðbundin skoðun

Keyrðu `python3 -m http.server 8000` úr þessari möppu.

## Birting

GitHub Pages birtir af `main`, úr rót geymslunnar. `CNAME` tengir hlustadu.is. Allar myndir og stílar eru hýst með síðunni.

## Myndir

- `assets/asgeir.jpg`: ljósmynd sem Ásgeir afhenti og heimilaði fyrir síðuna. K100 merki og skjár fjarlægð; bakgrunnur gerður sléttur gráblár með imagegen.
- `assets/studio.jpg` og `assets/location.jpg`: tímabundnar hugmyndamyndir gerðar með imagegen; skipta síðar út fyrir raunverulegar myndir af aðstöðu og búnaði.

## Samskipti

hlustadu@hlustadu.is · 659 2001. Sambandsform á forsíðunni býður texta eða allt að 90 sekúndna hljóðupptöku. Nafn og netfang eru nauðsynleg, sími valfrjáls. Netfang og sími eru áfram sýnileg.

`contact.js` heldur upptöku í vafranum þar til gestur sendir. `contact-config.js` inniheldur aðeins opinbert endpoint og Turnstile site key. Leynilykill er dulkóðaður sem `TURNSTILE_SECRET` hjá Cloudflare, aldrei í GitHub. Worker `hlustadu-contact` sannreynir Turnstile, leyfð upprunalén og stærð gagna, og sendir aðeins í staðfest pósthólf eiganda. Svarnetfang er netfang gestsins. Hljóð fylgir sem viðhengi (hámark 2,5 MB); engin sérstök skráageymsla eða gagnagrunnur.

Staðbundin forskoðun getur ekki sent með framleiðslulyklinum: Turnstile og bakendi leyfa hlustadu.is og www.hlustadu.is. Prófið sendingar á HTTPS-vefnum. Engar greiningarmælingar eru settar inn.

## Verð

Verðbirting bíður ákvörðunar Ásgeirs. 44.900 kr. + VSK er enn tillaga, ekki samþykkt verð.
