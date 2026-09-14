# alaveteli-dev への投稿（下書き・未送信）

宛先: https://groups.google.com/g/alaveteli-dev
※ 公開アーカイブに永久に残ります。送る前に内容をご確認ください。

---

**Subject:** Japanese (ja) translation ready — how to get it into Transifex?

Hi all,

I'm Atsushi Kojima, a developer in Nagoya, Japan.

I opened PR #9527 with a Japanese `app.po` (1,469 of 1,554 strings, no fuzzy entries).
Gareth kindly pointed me to Transifex, so I'd like to move it there.

What I have:

- `locale/ja/app.po` — placeholders (`{{name}}`), HTML tags, entities and URLs were
  machine-checked against each `msgid`
- Terminology follows the Japanese FOI system: request = 請求, public authority = 行政機関,
  successful = 開示, refused = 不開示, partially successful = 一部開示
- Checked on the Docker dev environment with `AVAILABLE_LOCALES: 'ja en'` and
  `DEFAULT_LOCALE: 'ja'`
- Screenshots: https://github.com/katsushi2441/alaveteli-jp/tree/jp/docs/screenshots

The remaining ~85 strings are help texts with nested `<strong>` markup. I left them for a
native reviewer rather than risk broken markup.

My question: the translation docs say to ask here about a Transifex account. Could someone
add me to the Japanese team on https://app.transifex.com/mysociety/alaveteli/ , or tell me
the right way to request it? My Transifex username is **katsushi2441** (same as GitHub).

On the other question from the PR thread — no, we are not running an Alaveteli instance in
Japan yet. Japan has a national FOI law (行政機関情報公開法) and prefectural ordinances, but
there is no WhatDoTheyKnow-style site. I translated the strings first so that the option
exists. If it goes live I'll let the community list know.

Thanks for maintaining Alaveteli.

Atsushi Kojima
EXBRIDGE, Inc. — Nagoya, Japan
https://github.com/katsushi2441
