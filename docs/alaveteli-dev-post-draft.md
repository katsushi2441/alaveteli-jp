# alaveteli-dev への投稿（**送信済み** 2026-09-15）

宛先: alaveteli-dev@googlegroups.com（https://groups.google.com/g/alaveteli-dev）
差出人: katsushi2441@gmail.com（対外メールの決まり）
送信済みトレイで確認済み。返事を待って、ja チームに入れてもらったら app.po を投入する。

**経緯**: 本家PR #9527 は 2026-09-14 にマージされずクローズ。拒否ではなく
「翻訳は Transifex から入れてほしい」という手続きの指示（garethrees）。
Transifex は**企業メール必須**だったので info@exbridge.jp で登録（ユーザー名 exbridge）。
GitHub は katsushi2441 で別名になるため、同一人物と分かる一文を本文に入れてある。

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
the right way to request it? My Transifex username is **exbridge** (I opened the PR as **@katsushi2441** on GitHub —
same person; Transifex wanted a company address so I signed up with our company one).

On the other question from the PR thread — no, we are not running an Alaveteli instance in
Japan yet. Japan has a national FOI law (行政機関情報公開法) and prefectural ordinances, but
there is no WhatDoTheyKnow-style site. I translated the strings first so that the option
exists. If it goes live I'll let the community list know.

Thanks for maintaining Alaveteli.

Atsushi Kojima
EXBRIDGE, Inc. — Nagoya, Japan
https://github.com/katsushi2441
