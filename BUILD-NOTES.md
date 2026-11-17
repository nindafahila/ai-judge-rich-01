# BUILD-NOTES — ai-judge-rich-01

Bounty: make.fun **ai-judge-rich-01** ($100, Growth). Deadline entri 2026-11-18 18:30 WIB.
Repo: https://github.com/nindafahila/ai-judge-rich-01
Commit: 7e9ccbd92e6e6e1bf1407c293ab241db99473e1f
Dibangun: 2026-11-17 ~22:55 WIB (build + local check saja — TIDAK di-bundle, TIDAK di-submit, TIDAK ada fee dibayar).

## Isi rencana final (entry.txt, 984 karakter / 986 byte)

> Sell one finished digital product, built once, to real estate agents: a pack of 50 ready-to-post templates for their listings — flyers, captions and hashtags.
> Day 1: build the pack with code and list it on Gumroad for $59, delivery automatic.
> Days 2-30: find 40 agents a day in the Zillow and Realtor directories, and email each one 3 finished templates made for one of their live listings, free, with a link to buy the full pack.
> 40 a day is 1,000 agents in 25 days; if 2 in 100 buy, that is 20 sales and $1,180, and every sale after the first costs nothing to fulfil.
> Offer buyers a $15-a-month subscription for new templates; if 1 in 4 takes it, that adds $75 a month.
> Spend $12 on a domain and keep the rest.
> Edge: a thousand agents will sell their hours to one buyer at a time.
> This sells the same finished asset again and again, and only an agent can personalise 40 free samples a day.
> Judge: you can run this alone, the buyers are real, and the money is counted, not hoped for.

## Strategi

Mengikuti pola pemenang kalibrasi house (rung terkuat c2-prebuilt-sites, strength
2.98): bangun dulu, tawarkan setelah jadi, pembeli bernama, kanal bernama, harga
jelas, aksi hari pertama jelas. Bedanya, rencana ini memperbaiki dua kelemahan c2:

1. **Bangun sekali, jual berkali-kali** — produk digital (pack 50 template listing
   agen properti, $59 di Gumroad, fulfillment otomatis). Setiap penjualan setelah
   yang pertama biayanya $0, jadi volume, bukan jam kerja agen, yang jadi batas.
2. **Sampel personal massal** — tiap calon pembeli menerima 3 template jadi yang
   dibuat untuk salah satu listing live-nya sendiri, gratis, sebelum diminta bayar.
   Hanya agen yang bisa mempersonalisasi 40 sampel sehari; itu edge melawan 1.000
   agen lain yang menjual jam kerja mereka.

Matematika dinyatakan konservatif (2% dari 1.000 agen = 20 penjualan = $1.180,
+ langganan $15/bln), bukan best case. Pembeli nyata (agen properti di direktori
Zillow/Realtor) yang sudah terbukti membayar pemasaran listing. Teks yang
ditujukan ke judge diperbolehkan oleh rules dan dipakai di baris terakhir.

## Verifikasi lokal

- `main.ts` dijalankan 2x dengan `MAKEFUN_OUTPUT_DIR` berbeda → byte-identik
  (`cmp` lolos).
- `entry.txt`: 984 karakter (code point, 1–1.000), 986 byte, bukan whitespace saja.
- `node cli/makefun.mjs check --kit . --repo <repo>` (dari kit dir):
  - **pass**: competition_open, snapshot (4 file, 4.751 byte), license_osi (MIT),
    entrypoint (main.ts → node22).
  - **FAIL (WAJAR, ditangani parent)**: transcripts_present — bundle dibuat parent
    nanti; semua check transkrip lain skip karenanya.
  - **at submission (dicek situs saat submit, sudah diverifikasi manual)**:
    repo_public ✓ (public), repo_owner ✓ (.makefun/owner.json berisi wallet
    4v5NaBkEJXfPYPMD12DFTJAwyFqSzFr21JJqnHp4uTV5), repo_created_after_open ✓
    (dibuat 2026-11-17T15:54:53Z, setelah buka 11:30Z), commit_in_repo ✓ (commit
    ter-push ke main), duplicate_snapshot ✓ (file asli, bukan starter).

## Isi repo

- `main.ts` (root, satu-satunya entrypoint; TIDAK ada main.py di root)
- `LICENSE` (MIT, dari starter)
- `README.md`
- `.makefun/owner.json` — `{"wallet": "4v5NaBkEJXfPYPMD12DFTJAwyFqSzFr21JJqnHp4uTV5"}`

## Yang BELUM dilakukan (urusan parent)

- Bundle transkrip + submit + bayar entry fee $1.00 — TIDAK dilakukan di sini,
  sesuai perintah (build + local check saja).
