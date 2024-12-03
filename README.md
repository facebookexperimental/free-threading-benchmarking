# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (dbd2379)](results/bm-20241123-3.14.0a2%2B-dbd2379-PYTHON_UOPS/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-01](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL) | python/7ea523f47cdb4cf512a1 | 7ea523f (NOGIL) | 1.199x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg) | 1.230x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg) | 1.247x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base.svg)[🧠](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base-mem.svg) |
| [2024-12-01](results/bm-20241201-3.14.0a2%2B-7ea523f) | python/7ea523f47cdb4cf512a1 | 7ea523f | 1.075x ↑<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-linux-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg) |  |
| [2024-11-30](results/bm-20241130-3.14.0a2%2B-328187c) | python/328187cc4fcdd578db42 | 328187c | 1.069x ↑<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg) |  |
| [2024-11-30](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL) | python/328187cc4fcdd578db42 | 328187c (NOGIL) | 1.209x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg) | 1.239x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg) | 1.251x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.svg)[🧠](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-linux-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base-mem.svg) |
| [2024-11-29](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL) | python/38264a060a8178d58046 | 38264a0 (NOGIL) | 1.196x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg) | 1.227x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg) | 1.242x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.svg)[🧠](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base-mem.svg) |
| [2024-11-29](results/bm-20241129-3.14.0a2%2B-38264a0) | python/38264a060a8178d58046 | 38264a0 | 1.070x ↑<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-linux-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-02](results/bm-20241202-3.14.0a2%2B-e517ccb) | nascheme/gh_115999_specialize | e517ccb | 1.030x ↑<br>[📄](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.12.6.md)[📈](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.12.6.svg) | 1.007x ↓<br>[📄](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.13.0rc2.md)[📈](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base.md)[📈](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base.svg)[🧠](results/bm-20241202-3.14.0a2%2B-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base-mem.svg) |
| [2024-12-01](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL) | python/7ea523f47cdb4cf512a1 | 7ea523f (NOGIL) | 1.261x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg) | 1.286x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg) | 1.277x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base.svg)[🧠](results/bm-20241201-3.14.0a2%2B-7ea523f-NOGIL/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-base-mem.svg) |
| [2024-12-01](results/bm-20241201-3.14.0a2%2B-7ea523f) | python/7ea523f47cdb4cf512a1 | 7ea523f | 1.033x ↑<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.12.6.svg) | 1.004x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.md)[📈](results/bm-20241201-3.14.0a2%2B-7ea523f/bm-20241201-vultr-x86_64-python-7ea523f47cdb4cf512a1-3.14.0a2%2B-7ea523f-vs-3.13.0rc2.svg) |  |
| [2024-12-01](results/bm-20241201-3.14.0a2%2B-f0b8a8f) | corona10/gh_115999_binary_sub | f0b8a8f | 1.036x ↑<br>[📄](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.12.6.md)[📈](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.13.0rc2.md)[📈](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base.md)[📈](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base.svg)[🧠](results/bm-20241201-3.14.0a2%2B-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base-mem.svg) |
| [2024-11-30](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL) | corona10/gh_115999_binary_sub | 0637d48 (NOGIL) | 1.254x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.12.6.md)[📈](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.12.6.svg) | 1.280x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.13.0rc2.md)[📈](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.13.0rc2.svg) | 1.012x ↑<br>[📄](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base.md)[📈](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base.svg)[🧠](results/bm-20241130-3.14.0a2%2B-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base-mem.svg) |
| [2024-11-30](results/bm-20241130-3.14.0a2%2B-328187c) | python/328187cc4fcdd578db42 | 328187c | 1.033x ↑<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg) |  |
| [2024-11-30](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL) | python/328187cc4fcdd578db42 | 328187c (NOGIL) | 1.254x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.12.6.svg) | 1.279x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-3.13.0rc2.svg) | 1.270x ↓<br>[📄](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.md)[📈](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base.svg)[🧠](results/bm-20241130-3.14.0a2%2B-328187c-NOGIL/bm-20241130-vultr-x86_64-python-328187cc4fcdd578db42-3.14.0a2%2B-328187c-vs-base-mem.svg) |
| [2024-11-29](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL) | python/38264a060a8178d58046 | 38264a0 (NOGIL) | 1.261x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg) | 1.286x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0-NOGIL/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg) |  |
| [2024-11-29](results/bm-20241129-3.14.0a2%2B-38264a0) | python/38264a060a8178d58046 | 38264a0 | 1.032x ↑<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.md)[📈](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base.svg)[🧠](results/bm-20241129-3.14.0a2%2B-38264a0/bm-20241129-vultr-x86_64-python-38264a060a8178d58046-3.14.0a2%2B-38264a0-vs-base-mem.svg) |
| [2024-11-29](results/bm-20241129-3.14.0a2%2B-15d6506) | python/15d6506d175780bb29e5 | 15d6506 | 1.031x ↑<br>[📄](results/bm-20241129-3.14.0a2%2B-15d6506/bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.md)[📈](results/bm-20241129-3.14.0a2%2B-15d6506/bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.12.6.svg) | 1.007x ↓<br>[📄](results/bm-20241129-3.14.0a2%2B-15d6506/bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.md)[📈](results/bm-20241129-3.14.0a2%2B-15d6506/bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2%2B-15d6506-vs-3.13.0rc2.svg) |  |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.

![Longitudinal speed improvement](/longitudinal.svg)

Improvement of the geometric mean of key merged benchmarks, computed with `pyperf compare`.
The results have a resolution of 0.01 (1%).

![Configuration speed improvement](/configs.svg)

## Documentation

### Running benchmarks from the GitHub web UI

Visit the 🔒 [benchmark action](../../actions/workflows/benchmark.yml) and click the "Run Workflow" button.

The available parameters are:

- `fork`: The fork of CPython to benchmark.
  If benchmarking a pull request, this would normally be your GitHub username.
- `ref`: The branch, tag or commit SHA to benchmark.
  If a SHA, it must be the full SHA, since finding it by a prefix is not supported.
- `machine`: The machine to run on.
  One of `linux-amd64` (default), `windows-amd64`, `darwin-arm64` or `all`.
- `benchmark_base`: If checked, the base of the selected branch will also be benchmarked.
  The base is determined by running `git merge-base upstream/main $ref`.
- `pystats`: If checked, collect the pystats from running the benchmarks.

To watch the progress of the benchmark, select it from the 🔒 [benchmark action page](../../actions/workflows/benchmark.yml).
It may be canceled from there as well.
To show only your benchmark workflows, select your GitHub ID from the "Actor" dropdown.

When the benchmarking is complete, the results are published to this repository and will appear in the [complete table](RESULTS.md).
Each set of benchmarks will have:

- The raw `.json` results from pyperformance.
- Comparisons against important reference releases, as well as the merge base of the branch if `benchmark_base` was selected. These include
  - A markdown table produced by `pyperf compare_to`.
  - A set of "violin" plots showing the distribution of results for each benchmark.

The most convenient way to get results locally is to clone this repo and `git pull` from it.

### Running benchmarks from the GitHub CLI

To automate benchmarking runs, it may be more convenient to use the [GitHub CLI](https://cli.github.com/).
Once you have `gh` installed and configured, you can run benchmarks by cloning this repository and then from inside it:

```bash session
gh workflow run benchmark.yml -f fork=me -f ref=my_branch
```

Any of the parameters described above are available at the commandline using the `-f key=value` syntax.

### Collecting Linux perf profiling data

To collect Linux perf sampling profile data for a benchmarking run, run the `_benchmark` action and check the `perf` checkbox.
Follow this by a run of the `_generate` action to regenerate the plots.

## License

This repo is licensed under the BSD 3-Clause License, as found in the LICENSE file.
