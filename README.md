
Hidden Crypto Miner for Monero — CPU Mining**

Runs on Linux and Windows x86-64, no library dependencies required.

**Builder:** builder.exe (Windows) or builder (Linux)
- Enter your Monero wallet address
- Select a pool from the list or specify a custom one
- "Save into binary" builds the miner

**Memory Modes:**
- **fast** — 2 GB dataset, maximum speed
- **light** — 256 MB cache, 3–4× slower, but works on low-end machines
- Hugepages (2 MB pages) are requested automatically; if privileges are insufficient, they fall back gracefully to regular pages.

**Pools:** Stratum+tcp
- Solo mode available via `monerod` JSON-RPC (`get_block_template` / `submit_block`).

**Load:** Defaults to 50 % of logical cores. Submitted shares are verified locally before being sent to the pool.

**Statistics:** Hashrate (H/s), total hashes, accepted/rejected shares 

**Diagnostics:** `--console` enables verbose message output.

**Auto-start** is built into the miner itself — no admin privileges required.

- Linux binary ≈ 1 MB
- Windows binary ≈ 3 MB

