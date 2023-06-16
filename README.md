<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

I fayn fɔ instɔl nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) fɔs, ɛn afta dat `direnv allow` afta yu dɔn ɛnta di dairektrɔ ( [di .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) go ɛksɛkutiv ɔtomɛtik afta yu ɛnta di dairektrɔ).

Di minin na: Chaynish transleshɔn to Japan, Korian, Inglish, Inglish transleshɔn to ɔl ɔda langwej dɛn. If yu jɔs want fɔ sɔpɔt Chaynish ɛn Inglish, yu kin jɔs rayt `zh: en` .

Di minin na: Chaynish transleshɔn to Japan, Korian, Inglish, Inglish transleshɔn to ɔl ɔda langwej dɛn. If yu jɔs want fɔ sɔpɔt Chaynish ɛn Inglish, yu kin jɔs rayt `zh: en` .

* [frɔnt-ɛnd kɔd](https://github.com/xxai-art/web)
* [Langwej pak fɔ di sayt as a ɔl](https://github.com/xxai-art/web/tree/main/i18n)
* [Langwej pak fɔ login modul dɛn](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Wɛbsayt Dɔkyumentri we gɛt bɔku langwej dɛn](https://github.com/xxai-doc)

Di frɔnt-ɛnd programin langwej na [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , we ad sɔm ficha dɛn bays pan di kɔfiskript sɛntaks, si [./coffee_plus.md](./coffee_plus.md) .

## Intanɛshɔnalayzeshɔn fɔ wɛbsayt ɛn dɔkyumɛnt dɛn

Bil pan di 3 prɔjek dɛn we de dɔŋ ya

* [@w5/mdt we de wok fɔ yu](https://www.npmjs.com/package/@w5/mdt)

  Di sɔfiks na `.mdt` , yu kin yuz di sɛntaks we fiba `<+ ./coffee_plus/import.js>` fɔ rifer to ɛksternal fayl dɛn, ɛn jenarayz makdɔwn wit di sɔfiks `.md` .

* [@w5/trmd we de sho aw fɔ du am](https://www.npmjs.com/package/@w5/trmd)

  Makdɔwn transleshɔn nɔ go translet kɔd ɛn link dɛn, ɛn i go kech di sɛntɛns dɛn we dɛn translet. If dɛn chenj di transleshɔn bɔt dɛn nɔ chenj di ɔrijinal tɛks, if yu du am bak, dat nɔ go rayt di chenj we dɛn chenj di transleshɔn.

* [@w5/i18n na di wan](https://www.npmjs.com/package/@w5/i18n)

  Langwej fayl fɔ translet `yaml` jenarayz wɛbsayt dɛn.

### Dokumɛnt Transleshɔn Ɔtomɛshɔn Instrɔkshɔn dɛn

Si di kɔd ripɔsitɔri [xxai-art/doc](https://github.com/xxai-art/doc)

I fayn fɔ instɔl nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) fɔs, ɛn afta dat `direnv allow` afta yu dɔn ɛnta di dairektrɔ ( [di .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) go ɛksɛkutiv ɔtomɛtik afta yu ɛnta di dairektrɔ).

Fɔ mek a nɔ gɛt di big kɔd bays we dɛn translet to ɔndrɛd langwej dɛn, a mek wan sɛpret kɔd bays fɔ ɛni langwej ɛn mek wan ɔganayzeshɔn fɔ kip di kɔd bays

We yu sɛt di envayrɔmɛnt vɛriɔbul `GITHUB_ACCESS_TOKEN` ɛn afta dat yu rɔn [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) i go mek di kɔd ripɔsitɔri ɔtomɛtik wan.

Na tru se yu kin put am bak na kɔd bays.

Transleshɔn skript rɛfrɛns [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Dɛn kin ɛksplen di skript kɔd lɛk dis:

[bunx](https://bun.sh/docs/cli/bunx) na riplesmɛnt fɔ npx, we fast pas ɔl. Na tru se if yu nɔ gɛt bun instɔl, yu kin yuz `npx` insted.

`bunx mdt zh` de rɛnd `.mdt` na di zh dairektrɔ as `.md` , si di 2 linked fayl dɛn dɔŋ ya

* [kɔfi_plɔs.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [kɔfi_plɔs.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` na di kor kod fo transleshon (if yu onli geht `nodejs` inshol, bot `bun` en `direnv` no inshol, yu kin ron `npx i18n` tu fo translet).

I go parse [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , di kɔnfigyushɔn fɔ `i18n.yml` na dis dɔkyumɛnt na lɛk dis:

```
en:
zh: ja ko en
```

Di minin na: Chaynish transleshɔn to Japan, Korian, Inglish, Inglish transleshɔn to ɔl ɔda langwej dɛn. If yu jɔs want fɔ sɔpɔt Chaynish ɛn Inglish, yu kin jɔs rayt `zh: en` .

Di las wan na [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , we de pul di tin dɛn we de insay bitwin di men taytul ɛn di fɔs sabtaytul fɔ ɛni langwej in `README.md` fɔ mek wan ɛntri `README.md` . Di kɔd rili simpul, yu kin luk am yusɛf.

Dɛn kin yuz Google API fɔ fri transleshɔn. If yu nɔ ebul fɔ akses Google, duya kɔnfigyut ɛn sɛt prɔksi, lɛk:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Di transleshɔn skript go jenarayz wan translet kesh na `.i18n` dairektrɔ, duya chɛk am wit `git status` ɛn ad am to di kɔd ripɔsitɔri fɔ avɔyd ripit transleshɔn.

Duya, rɔn `bunx i18n` ɛvri tɛm we yu chenj di transleshɔn fɔ ɔpdet di kesh.

If dɛn chenj di ɔrijinal tɛks ɛn di transleshɔn di sem tɛm, di kesh go kɔnfyus, so if yu want fɔ chenj, yu kin jɔs chenj wan, dɔn yu kin rɔn `bunx i18n` fɔ ɔpdet di kesh.
