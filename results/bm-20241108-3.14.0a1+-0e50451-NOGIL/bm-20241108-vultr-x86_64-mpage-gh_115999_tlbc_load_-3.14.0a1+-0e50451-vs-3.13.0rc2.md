# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 410 ms: 1.58x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.31 sec: 1.27x slower                                                |
| html5lib       | 67.0 ms                                                      | 105 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 581 ms: 1.15x slower                                                  |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                                |
| coroutines       | 23.6 ms                                                      | 28.9 ms: 1.23x slower                                                 |
| async_generators | 377 ms                                                       | 480 ms: 1.27x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.17x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                                  |
| float          | 77.5 ms                                                      | 149 ms: 1.93x slower                                                  |
| nbody          | 85.1 ms                                                      | 199 ms: 2.34x slower                                                  |
| Geometric mean | (ref)                                                        | 1.56x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.20 ms: 1.04x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                 |
| regex_compile  | 132 ms                                                       | 212 ms: 1.60x slower                                                  |
| Geometric mean | (ref)                                                        | 1.17x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| pickle_list          | 4.93 us                                                      | 5.13 us: 1.04x slower                                                 |
| pickle               | 11.3 us                                                      | 12.0 us: 1.06x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.01 us: 1.06x slower                                                 |
| json_loads           | 27.0 us                                                      | 29.4 us: 1.09x slower                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 106 ms: 1.12x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 109 ms: 1.28x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 14.7 ms: 1.40x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 89.3 ms: 1.51x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 3.12 sec: 1.55x slower                                                |
| unpickle_pure_python | 210 us                                                       | 389 us: 1.85x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 577 us: 1.96x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 74.3 ms: 1.52x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                 |
| django_template | 34.1 ms                                                      | 59.2 ms: 1.73x slower                                                 |
| mako            | 11.3 ms                                                      | 20.2 ms: 1.78x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.68x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.46 ms: 1.28x faster                                                 |
| create_gc_cycles         | 1.34 ms                                                      | 1.11 ms: 1.20x faster                                                 |
| pidigits                 | 217 ms                                                       | 182 ms: 1.19x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.6 us: 1.03x faster                                                 |
| xml_etree_parse          | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| regex_dna                | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_effbot             | 3.08 ms                                                      | 3.20 ms: 1.04x slower                                                 |
| pickle_list              | 4.93 us                                                      | 5.13 us: 1.04x slower                                                 |
| pickle                   | 11.3 us                                                      | 12.0 us: 1.06x slower                                                 |
| unpickle_list            | 4.71 us                                                      | 5.01 us: 1.06x slower                                                 |
| json                     | 4.93 ms                                                      | 5.35 ms: 1.09x slower                                                 |
| json_loads               | 27.0 us                                                      | 29.4 us: 1.09x slower                                                 |
| deepcopy                 | 355 us                                                       | 387 us: 1.09x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.43 us: 1.10x slower                                                 |
| regex_v8                 | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                 |
| pathlib                  | 19.2 ms                                                      | 21.4 ms: 1.11x slower                                                 |
| xml_etree_iterparse      | 94.9 ms                                                      | 106 ms: 1.12x slower                                                  |
| asyncio_tcp              | 505 ms                                                       | 581 ms: 1.15x slower                                                  |
| scimark_fft              | 349 ms                                                       | 410 ms: 1.17x slower                                                  |
| telco                    | 7.82 ms                                                      | 9.19 ms: 1.17x slower                                                 |
| deepcopy_memo            | 39.1 us                                                      | 46.7 us: 1.20x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                                |
| coverage                 | 83.0 ms                                                      | 101 ms: 1.22x slower                                                  |
| coroutines               | 23.6 ms                                                      | 28.9 ms: 1.23x slower                                                 |
| docutils                 | 2.62 sec                                                     | 3.31 sec: 1.27x slower                                                |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.97 ms: 1.27x slower                                                 |
| async_generators         | 377 ms                                                       | 480 ms: 1.27x slower                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 109 ms: 1.28x slower                                                  |
| pylint                   | 317 ms                                                       | 409 ms: 1.29x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 5.79 sec: 1.30x slower                                                |
| deepcopy_reduce          | 3.11 us                                                      | 4.10 us: 1.32x slower                                                 |
| meteor_contest           | 102 ms                                                       | 136 ms: 1.33x slower                                                  |
| mdp                      | 2.36 sec                                                     | 3.19 sec: 1.36x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.37x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 14.7 ms: 1.40x slower                                                 |
| spectral_norm            | 111 ms                                                       | 156 ms: 1.40x slower                                                  |
| python_startup           | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                 |
| nqueens                  | 78.6 ms                                                      | 112 ms: 1.43x slower                                                  |
| generators               | 28.8 ms                                                      | 41.3 ms: 1.43x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 226 us: 1.46x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.68 sec: 1.50x slower                                                |
| xml_etree_process        | 59.3 ms                                                      | 89.3 ms: 1.51x slower                                                 |
| fannkuch                 | 370 ms                                                       | 562 ms: 1.52x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 74.3 ms: 1.52x slower                                                 |
| tomli_loads              | 2.01 sec                                                     | 3.12 sec: 1.55x slower                                                |
| sqlglot_normalize        | 106 ms                                                       | 164 ms: 1.56x slower                                                  |
| sqlglot_optimize         | 52.7 ms                                                      | 82.1 ms: 1.56x slower                                                 |
| html5lib                 | 67.0 ms                                                      | 105 ms: 1.57x slower                                                  |
| 2to3                     | 260 ms                                                       | 410 ms: 1.58x slower                                                  |
| pprint_safe_repr         | 738 ms                                                       | 1.17 sec: 1.58x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.59x slower                                                  |
| regex_compile            | 132 ms                                                       | 212 ms: 1.60x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.42 sec: 1.62x slower                                                |
| sympy_integrate          | 19.8 ms                                                      | 32.2 ms: 1.63x slower                                                 |
| thrift                   | 778 us                                                       | 1.27 ms: 1.63x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                 |
| pyflate                  | 449 ms                                                       | 758 ms: 1.69x slower                                                  |
| django_template          | 34.1 ms                                                      | 59.2 ms: 1.73x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.2 ms: 1.78x slower                                                 |
| comprehensions           | 16.5 us                                                      | 29.8 us: 1.81x slower                                                 |
| unpickle_pure_python     | 210 us                                                       | 389 us: 1.85x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 124 ms: 1.90x slower                                                  |
| logging_format           | 6.84 us                                                      | 13.1 us: 1.91x slower                                                 |
| richards                 | 45.2 ms                                                      | 86.7 ms: 1.92x slower                                                 |
| scimark_lu               | 113 ms                                                       | 216 ms: 1.92x slower                                                  |
| sympy_str                | 275 ms                                                       | 527 ms: 1.92x slower                                                  |
| logging_simple           | 6.16 us                                                      | 11.8 us: 1.92x slower                                                 |
| float                    | 77.5 ms                                                      | 149 ms: 1.93x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 577 us: 1.96x slower                                                  |
| hexiom                   | 5.99 ms                                                      | 11.8 ms: 1.97x slower                                                 |
| richards_super           | 51.6 ms                                                      | 104 ms: 2.01x slower                                                  |
| scimark_sor              | 134 ms                                                       | 271 ms: 2.01x slower                                                  |
| logging_silent           | 103 ns                                                       | 208 ns: 2.02x slower                                                  |
| go                       | 141 ms                                                       | 292 ms: 2.08x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 3.24 ms: 2.08x slower                                                 |
| chaos                    | 57.3 ms                                                      | 119 ms: 2.08x slower                                                  |
| sympy_expand             | 457 ms                                                       | 1.03 sec: 2.26x slower                                                |
| sqlglot_parse            | 1.25 ms                                                      | 2.82 ms: 2.26x slower                                                 |
| nbody                    | 85.1 ms                                                      | 199 ms: 2.34x slower                                                  |
| sympy_sum                | 156 ms                                                       | 372 ms: 2.39x slower                                                  |
| raytrace                 | 253 ms                                                       | 637 ms: 2.52x slower                                                  |
| deltablue                | 3.12 ms                                                      | 8.90 ms: 2.85x slower                                                 |
| unpack_sequence          | 44.8 ns                                                      | 137 ns: 3.06x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 3.46 ms: 3.76x slower                                                 |
| bench_mp_pool            | 11.0 ms                                                      | 72.1 ms: 6.55x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.52x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, unpickle
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.43x
- 95% likely to have a slowdown of 1.41x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.22x