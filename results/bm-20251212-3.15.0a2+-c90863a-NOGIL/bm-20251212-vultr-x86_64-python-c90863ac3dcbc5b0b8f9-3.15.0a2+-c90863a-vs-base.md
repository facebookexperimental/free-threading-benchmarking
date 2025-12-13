# Results vs. base

- fork: python
- ref: c90863ac3dcbc5b0b8f9
- machine: linux-x86_64
- commit hash: c90863a
- commit date: 2025-12-12
- overall geometric mean: 1.106x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 244 ms                                                                                                            | 279 ms: 1.14x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 2.76 sec: 1.09x slower                                                                                                  |
| html5lib       | 59.0 ms                                                                                                           | 67.4 ms: 1.14x slower                                                                                                   |
| sphinx         | 971 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 543 ms                                                                                                            | 511 ms: 1.06x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                            | 521 ms: 1.03x slower                                                                                                    |
| async_tree_io_tg           | 587 ms                                                                                                            | 621 ms: 1.06x slower                                                                                                    |
| async_tree_memoization_tg  | 305 ms                                                                                                            | 328 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 502 ms                                                                                                            | 547 ms: 1.09x slower                                                                                                    |
| async_tree_none_tg         | 243 ms                                                                                                            | 264 ms: 1.09x slower                                                                                                    |
| async_generators           | 339 ms                                                                                                            | 375 ms: 1.11x slower                                                                                                    |
| async_tree_io              | 550 ms                                                                                                            | 628 ms: 1.14x slower                                                                                                    |
| async_tree_none            | 242 ms                                                                                                            | 287 ms: 1.18x slower                                                                                                    |
| async_tree_memoization     | 300 ms                                                                                                            | 355 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                                                            | 190 ms: 1.13x faster                                                                                                    |
| float          | 69.5 ms                                                                                                           | 72.0 ms: 1.04x slower                                                                                                   |
| nbody          | 86.7 ms                                                                                                           | 122 ms: 1.40x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.9 ms                                                                                                           | 21.4 ms: 1.07x faster                                                                                                   |
| regex_dna      | 177 ms                                                                                                            | 178 ms: 1.01x slower                                                                                                    |
| regex_effbot   | 2.83 ms                                                                                                           | 2.87 ms: 1.01x slower                                                                                                   |
| regex_compile  | 124 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 134 ms: 1.03x slower                                                                                                    |
| xml_etree_iterparse  | 84.2 ms                                                                                                           | 88.3 ms: 1.05x slower                                                                                                   |
| tomli_loads          | 2.17 sec                                                                                                          | 2.29 sec: 1.06x slower                                                                                                  |
| pickle_pure_python   | 309 us                                                                                                            | 337 us: 1.09x slower                                                                                                    |
| unpickle_pure_python | 213 us                                                                                                            | 237 us: 1.11x slower                                                                                                    |
| json_dumps           | 9.90 ms                                                                                                           | 11.2 ms: 1.13x slower                                                                                                   |
| json_loads           | 27.6 us                                                                                                           | 31.2 us: 1.13x slower                                                                                                   |
| xml_etree_generate   | 82.4 ms                                                                                                           | 98.8 ms: 1.20x slower                                                                                                   |
| xml_etree_process    | 57.7 ms                                                                                                           | 70.6 ms: 1.22x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.29 ms                                                                                                           | 9.70 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                                                           | 40.8 ms: 1.14x slower                                                                                                   |
| genshi_xml      | 48.9 ms                                                                                                           | 58.9 ms: 1.20x slower                                                                                                   |
| genshi_text     | 20.7 ms                                                                                                           | 26.5 ms: 1.28x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 15.4 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20251212-3.15.0a2+-c90863a/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json | results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 282 ms                                                                                                            | 7.14 ms: 39.46x faster                                                                                                  |
| gc_traversal               | 4.00 ms                                                                                                           | 1.93 ms: 2.08x faster                                                                                                   |
| create_gc_cycles           | 1.87 ms                                                                                                           | 1.51 ms: 1.24x faster                                                                                                   |
| pidigits                   | 215 ms                                                                                                            | 190 ms: 1.13x faster                                                                                                    |
| sqlite_synth               | 2.27 us                                                                                                           | 2.05 us: 1.11x faster                                                                                                   |
| regex_v8                   | 22.9 ms                                                                                                           | 21.4 ms: 1.07x faster                                                                                                   |
| asyncio_websockets         | 543 ms                                                                                                            | 511 ms: 1.06x faster                                                                                                    |
| pycparser                  | 1.12 sec                                                                                                          | 1.13 sec: 1.01x slower                                                                                                  |
| regex_dna                  | 177 ms                                                                                                            | 178 ms: 1.01x slower                                                                                                    |
| regex_effbot               | 2.83 ms                                                                                                           | 2.87 ms: 1.01x slower                                                                                                   |
| xml_etree_parse            | 130 ms                                                                                                            | 134 ms: 1.03x slower                                                                                                    |
| logging_silent             | 99.8 ns                                                                                                           | 103 ns: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                            | 521 ms: 1.03x slower                                                                                                    |
| pathlib                    | 17.6 ms                                                                                                           | 18.2 ms: 1.03x slower                                                                                                   |
| float                      | 69.5 ms                                                                                                           | 72.0 ms: 1.04x slower                                                                                                   |
| xml_etree_iterparse        | 84.2 ms                                                                                                           | 88.3 ms: 1.05x slower                                                                                                   |
| bpe_tokeniser              | 4.16 sec                                                                                                          | 4.38 sec: 1.05x slower                                                                                                  |
| tomli_loads                | 2.17 sec                                                                                                          | 2.29 sec: 1.06x slower                                                                                                  |
| async_tree_io_tg           | 587 ms                                                                                                            | 621 ms: 1.06x slower                                                                                                    |
| json                       | 5.03 ms                                                                                                           | 5.37 ms: 1.07x slower                                                                                                   |
| async_tree_memoization_tg  | 305 ms                                                                                                            | 328 ms: 1.07x slower                                                                                                    |
| dulwich_log                | 67.0 ms                                                                                                           | 72.1 ms: 1.08x slower                                                                                                   |
| generators                 | 28.6 ms                                                                                                           | 30.8 ms: 1.08x slower                                                                                                   |
| deltablue                  | 3.38 ms                                                                                                           | 3.65 ms: 1.08x slower                                                                                                   |
| docutils                   | 2.54 sec                                                                                                          | 2.76 sec: 1.09x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 502 ms                                                                                                            | 547 ms: 1.09x slower                                                                                                    |
| pickle_pure_python         | 309 us                                                                                                            | 337 us: 1.09x slower                                                                                                    |
| async_tree_none_tg         | 243 ms                                                                                                            | 264 ms: 1.09x slower                                                                                                    |
| pylint                     | 282 ms                                                                                                            | 307 ms: 1.09x slower                                                                                                    |
| sympy_expand               | 482 ms                                                                                                            | 529 ms: 1.10x slower                                                                                                    |
| sphinx                     | 971 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| nqueens                    | 78.8 ms                                                                                                           | 86.6 ms: 1.10x slower                                                                                                   |
| pyflate                    | 413 ms                                                                                                            | 455 ms: 1.10x slower                                                                                                    |
| many_optionals             | 946 us                                                                                                            | 1.04 ms: 1.10x slower                                                                                                   |
| async_generators           | 339 ms                                                                                                            | 375 ms: 1.11x slower                                                                                                    |
| unpickle_pure_python       | 213 us                                                                                                            | 237 us: 1.11x slower                                                                                                    |
| scimark_fft                | 304 ms                                                                                                            | 341 ms: 1.12x slower                                                                                                    |
| bench_thread_pool          | 1.32 ms                                                                                                           | 1.48 ms: 1.12x slower                                                                                                   |
| json_dumps                 | 9.90 ms                                                                                                           | 11.2 ms: 1.13x slower                                                                                                   |
| subparsers                 | 9.09 ms                                                                                                           | 10.3 ms: 1.13x slower                                                                                                   |
| telco                      | 158 ms                                                                                                            | 178 ms: 1.13x slower                                                                                                    |
| json_loads                 | 27.6 us                                                                                                           | 31.2 us: 1.13x slower                                                                                                   |
| comprehensions             | 15.8 us                                                                                                           | 18.0 us: 1.14x slower                                                                                                   |
| deepcopy_reduce            | 2.63 us                                                                                                           | 2.98 us: 1.14x slower                                                                                                   |
| deepcopy_memo              | 26.9 us                                                                                                           | 30.6 us: 1.14x slower                                                                                                   |
| chaos                      | 55.2 ms                                                                                                           | 62.7 ms: 1.14x slower                                                                                                   |
| pprint_safe_repr           | 698 ms                                                                                                            | 795 ms: 1.14x slower                                                                                                    |
| spectral_norm              | 96.5 ms                                                                                                           | 110 ms: 1.14x slower                                                                                                    |
| django_template            | 35.8 ms                                                                                                           | 40.8 ms: 1.14x slower                                                                                                   |
| sympy_str                  | 274 ms                                                                                                            | 313 ms: 1.14x slower                                                                                                    |
| 2to3                       | 244 ms                                                                                                            | 279 ms: 1.14x slower                                                                                                    |
| scimark_sor                | 108 ms                                                                                                            | 123 ms: 1.14x slower                                                                                                    |
| html5lib                   | 59.0 ms                                                                                                           | 67.4 ms: 1.14x slower                                                                                                   |
| async_tree_io              | 550 ms                                                                                                            | 628 ms: 1.14x slower                                                                                                    |
| mdp                        | 1.16 sec                                                                                                          | 1.32 sec: 1.14x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| deepcopy                   | 242 us                                                                                                            | 278 us: 1.15x slower                                                                                                    |
| sympy_sum                  | 155 ms                                                                                                            | 178 ms: 1.15x slower                                                                                                    |
| hexiom                     | 5.60 ms                                                                                                           | 6.44 ms: 1.15x slower                                                                                                   |
| sympy_integrate            | 18.9 ms                                                                                                           | 21.8 ms: 1.15x slower                                                                                                   |
| fannkuch                   | 393 ms                                                                                                            | 454 ms: 1.16x slower                                                                                                    |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 117 ms: 1.16x slower                                                                                                    |
| go                         | 105 ms                                                                                                            | 121 ms: 1.16x slower                                                                                                    |
| pprint_pformat             | 1.42 sec                                                                                                          | 1.65 sec: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.6 ms                                                                                                           | 59.0 ms: 1.17x slower                                                                                                   |
| thrift                     | 767 us                                                                                                            | 897 us: 1.17x slower                                                                                                    |
| async_tree_none            | 242 ms                                                                                                            | 287 ms: 1.18x slower                                                                                                    |
| async_tree_memoization     | 300 ms                                                                                                            | 355 ms: 1.19x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.28 ms                                                                                                           | 5.08 ms: 1.19x slower                                                                                                   |
| raytrace                   | 250 ms                                                                                                            | 296 ms: 1.19x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                           | 1.78 ms: 1.20x slower                                                                                                   |
| meteor_contest             | 101 ms                                                                                                            | 121 ms: 1.20x slower                                                                                                    |
| xml_etree_generate         | 82.4 ms                                                                                                           | 98.8 ms: 1.20x slower                                                                                                   |
| k_core                     | 1.87 sec                                                                                                          | 2.24 sec: 1.20x slower                                                                                                  |
| genshi_xml                 | 48.9 ms                                                                                                           | 58.9 ms: 1.20x slower                                                                                                   |
| scimark_lu                 | 107 ms                                                                                                            | 131 ms: 1.22x slower                                                                                                    |
| logging_simple             | 5.70 us                                                                                                           | 6.96 us: 1.22x slower                                                                                                   |
| xml_etree_process          | 57.7 ms                                                                                                           | 70.6 ms: 1.22x slower                                                                                                   |
| sqlglot_v2_parse           | 1.19 ms                                                                                                           | 1.45 ms: 1.22x slower                                                                                                   |
| logging_format             | 6.44 us                                                                                                           | 7.91 us: 1.23x slower                                                                                                   |
| richards                   | 42.4 ms                                                                                                           | 52.1 ms: 1.23x slower                                                                                                   |
| scimark_monte_carlo        | 63.2 ms                                                                                                           | 77.9 ms: 1.23x slower                                                                                                   |
| richards_super             | 48.4 ms                                                                                                           | 59.7 ms: 1.23x slower                                                                                                   |
| shortest_path              | 429 ms                                                                                                            | 530 ms: 1.24x slower                                                                                                    |
| crypto_pyaes               | 68.9 ms                                                                                                           | 85.5 ms: 1.24x slower                                                                                                   |
| connected_components       | 385 ms                                                                                                            | 481 ms: 1.25x slower                                                                                                    |
| python_startup             | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| genshi_text                | 20.7 ms                                                                                                           | 26.5 ms: 1.28x slower                                                                                                   |
| typing_runtime_protocols   | 153 us                                                                                                            | 196 us: 1.29x slower                                                                                                    |
| mako                       | 11.8 ms                                                                                                           | 15.4 ms: 1.31x slower                                                                                                   |
| python_startup_no_site     | 7.29 ms                                                                                                           | 9.70 ms: 1.33x slower                                                                                                   |
| coverage                   | 82.8 ms                                                                                                           | 111 ms: 1.34x slower                                                                                                    |
| nbody                      | 86.7 ms                                                                                                           | 122 ms: 1.40x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): coroutines

- Geometric mean (including insignificant results): 1.106x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x