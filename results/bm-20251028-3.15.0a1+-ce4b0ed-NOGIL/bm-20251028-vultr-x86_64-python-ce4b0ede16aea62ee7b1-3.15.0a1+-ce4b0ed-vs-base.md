# Results vs. base

- fork: python
- ref: ce4b0ede16aea62ee7b1
- machine: linux-x86_64
- commit hash: ce4b0ed
- commit date: 2025-10-28
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.71 sec: 1.06x slower                                                                                                  |
| html5lib       | 61.0 ms                                                                                                           | 65.8 ms: 1.08x slower                                                                                                   |
| sphinx         | 968 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 594 ms                                                                                                            | 519 ms: 1.15x faster                                                                                                    |
| async_tree_none_tg        | 250 ms                                                                                                            | 226 ms: 1.10x faster                                                                                                    |
| async_tree_memoization_tg | 310 ms                                                                                                            | 285 ms: 1.09x faster                                                                                                    |
| asyncio_websockets        | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| async_tree_io             | 555 ms                                                                                                            | 545 ms: 1.02x faster                                                                                                    |
| coroutines                | 24.3 ms                                                                                                           | 23.9 ms: 1.02x faster                                                                                                   |
| async_tree_none           | 248 ms                                                                                                            | 257 ms: 1.04x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 484 ms                                                                                                            | 518 ms: 1.07x slower                                                                                                    |
| async_generators          | 339 ms                                                                                                            | 376 ms: 1.11x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                                                                            | 196 ms: 1.01x slower                                                                                                    |
| nbody          | 92.9 ms                                                                                                           | 126 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                                                                           | 21.3 ms: 1.05x faster                                                                                                   |
| regex_dna      | 173 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| regex_effbot   | 2.68 ms                                                                                                           | 2.96 ms: 1.11x slower                                                                                                   |
| regex_compile  | 123 ms                                                                                                            | 143 ms: 1.16x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 132 ms: 1.02x slower                                                                                                    |
| xml_etree_iterparse  | 85.2 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| tomli_loads          | 1.88 sec                                                                                                          | 2.02 sec: 1.07x slower                                                                                                  |
| pickle_pure_python   | 307 us                                                                                                            | 337 us: 1.10x slower                                                                                                    |
| unpickle_pure_python | 210 us                                                                                                            | 233 us: 1.11x slower                                                                                                    |
| json_loads           | 28.3 us                                                                                                           | 31.5 us: 1.12x slower                                                                                                   |
| json_dumps           | 9.68 ms                                                                                                           | 11.2 ms: 1.15x slower                                                                                                   |
| xml_etree_generate   | 82.9 ms                                                                                                           | 95.8 ms: 1.16x slower                                                                                                   |
| xml_etree_process    | 59.2 ms                                                                                                           | 68.9 ms: 1.16x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.7 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.22 ms                                                                                                           | 9.58 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 33.9 ms                                                                                                           | 40.0 ms: 1.18x slower                                                                                                   |
| genshi_xml      | 47.5 ms                                                                                                           | 58.6 ms: 1.23x slower                                                                                                   |
| genshi_text     | 20.5 ms                                                                                                           | 26.5 ms: 1.29x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 15.5 ms: 1.34x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.26x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20251028-3.15.0a1+-ce4b0ed/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json | results/bm-20251028-3.15.0a1+-ce4b0ed-NOGIL/bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1+-ce4b0ed.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal              | 4.67 ms                                                                                                           | 1.93 ms: 2.41x faster                                                                                                   |
| create_gc_cycles          | 1.93 ms                                                                                                           | 1.50 ms: 1.29x faster                                                                                                   |
| async_tree_io_tg          | 594 ms                                                                                                            | 519 ms: 1.15x faster                                                                                                    |
| sqlite_synth              | 2.26 us                                                                                                           | 2.03 us: 1.11x faster                                                                                                   |
| async_tree_none_tg        | 250 ms                                                                                                            | 226 ms: 1.10x faster                                                                                                    |
| async_tree_memoization_tg | 310 ms                                                                                                            | 285 ms: 1.09x faster                                                                                                    |
| asyncio_websockets        | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| regex_v8                  | 22.3 ms                                                                                                           | 21.3 ms: 1.05x faster                                                                                                   |
| async_tree_io             | 555 ms                                                                                                            | 545 ms: 1.02x faster                                                                                                    |
| coroutines                | 24.3 ms                                                                                                           | 23.9 ms: 1.02x faster                                                                                                   |
| pathlib                   | 17.7 ms                                                                                                           | 17.9 ms: 1.01x slower                                                                                                   |
| pidigits                  | 194 ms                                                                                                            | 196 ms: 1.01x slower                                                                                                    |
| xml_etree_parse           | 130 ms                                                                                                            | 132 ms: 1.02x slower                                                                                                    |
| xml_etree_iterparse       | 85.2 ms                                                                                                           | 88.2 ms: 1.04x slower                                                                                                   |
| async_tree_none           | 248 ms                                                                                                            | 257 ms: 1.04x slower                                                                                                    |
| logging_silent            | 100 ns                                                                                                            | 104 ns: 1.04x slower                                                                                                    |
| bpe_tokeniser             | 4.23 sec                                                                                                          | 4.45 sec: 1.05x slower                                                                                                  |
| regex_dna                 | 173 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| pycparser                 | 1.07 sec                                                                                                          | 1.13 sec: 1.06x slower                                                                                                  |
| pylint                    | 287 ms                                                                                                            | 305 ms: 1.06x slower                                                                                                    |
| docutils                  | 2.55 sec                                                                                                          | 2.71 sec: 1.06x slower                                                                                                  |
| dulwich_log               | 68.0 ms                                                                                                           | 72.5 ms: 1.07x slower                                                                                                   |
| async_tree_cpu_io_mixed   | 484 ms                                                                                                            | 518 ms: 1.07x slower                                                                                                    |
| tomli_loads               | 1.88 sec                                                                                                          | 2.02 sec: 1.07x slower                                                                                                  |
| json                      | 5.01 ms                                                                                                           | 5.38 ms: 1.07x slower                                                                                                   |
| html5lib                  | 61.0 ms                                                                                                           | 65.8 ms: 1.08x slower                                                                                                   |
| sympy_expand              | 476 ms                                                                                                            | 519 ms: 1.09x slower                                                                                                    |
| pickle_pure_python        | 307 us                                                                                                            | 337 us: 1.10x slower                                                                                                    |
| pprint_safe_repr          | 707 ms                                                                                                            | 777 ms: 1.10x slower                                                                                                    |
| sphinx                    | 968 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| many_optionals            | 1.23 ms                                                                                                           | 1.35 ms: 1.10x slower                                                                                                   |
| nqueens                   | 80.4 ms                                                                                                           | 88.7 ms: 1.10x slower                                                                                                   |
| telco                     | 157 ms                                                                                                            | 174 ms: 1.11x slower                                                                                                    |
| async_generators          | 339 ms                                                                                                            | 376 ms: 1.11x slower                                                                                                    |
| regex_effbot              | 2.68 ms                                                                                                           | 2.96 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python      | 210 us                                                                                                            | 233 us: 1.11x slower                                                                                                    |
| pyflate                   | 417 ms                                                                                                            | 465 ms: 1.11x slower                                                                                                    |
| json_loads                | 28.3 us                                                                                                           | 31.5 us: 1.12x slower                                                                                                   |
| pprint_pformat            | 1.44 sec                                                                                                          | 1.61 sec: 1.12x slower                                                                                                  |
| chaos                     | 56.4 ms                                                                                                           | 63.5 ms: 1.13x slower                                                                                                   |
| 2to3                      | 248 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| scimark_fft               | 310 ms                                                                                                            | 351 ms: 1.13x slower                                                                                                    |
| sympy_str                 | 273 ms                                                                                                            | 309 ms: 1.13x slower                                                                                                    |
| scimark_sor               | 109 ms                                                                                                            | 123 ms: 1.14x slower                                                                                                    |
| deepcopy                  | 244 us                                                                                                            | 278 us: 1.14x slower                                                                                                    |
| mdp                       | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| hexiom                    | 5.65 ms                                                                                                           | 6.44 ms: 1.14x slower                                                                                                   |
| sqlglot_v2_normalize      | 100 ms                                                                                                            | 115 ms: 1.14x slower                                                                                                    |
| deepcopy_reduce           | 2.58 us                                                                                                           | 2.96 us: 1.15x slower                                                                                                   |
| spectral_norm             | 96.6 ms                                                                                                           | 111 ms: 1.15x slower                                                                                                    |
| comprehensions            | 15.7 us                                                                                                           | 18.0 us: 1.15x slower                                                                                                   |
| sympy_sum                 | 153 ms                                                                                                            | 176 ms: 1.15x slower                                                                                                    |
| sqlglot_v2_optimize       | 50.5 ms                                                                                                           | 58.0 ms: 1.15x slower                                                                                                   |
| go                        | 106 ms                                                                                                            | 121 ms: 1.15x slower                                                                                                    |
| sympy_integrate           | 19.0 ms                                                                                                           | 21.8 ms: 1.15x slower                                                                                                   |
| json_dumps                | 9.68 ms                                                                                                           | 11.2 ms: 1.15x slower                                                                                                   |
| xml_etree_generate        | 82.9 ms                                                                                                           | 95.8 ms: 1.16x slower                                                                                                   |
| regex_compile             | 123 ms                                                                                                            | 143 ms: 1.16x slower                                                                                                    |
| subparsers                | 44.2 ms                                                                                                           | 51.4 ms: 1.16x slower                                                                                                   |
| fannkuch                  | 394 ms                                                                                                            | 458 ms: 1.16x slower                                                                                                    |
| xml_etree_process         | 59.2 ms                                                                                                           | 68.9 ms: 1.16x slower                                                                                                   |
| deepcopy_memo             | 26.4 us                                                                                                           | 31.0 us: 1.17x slower                                                                                                   |
| sqlglot_v2_transpile      | 1.51 ms                                                                                                           | 1.78 ms: 1.18x slower                                                                                                   |
| logging_simple            | 5.75 us                                                                                                           | 6.76 us: 1.18x slower                                                                                                   |
| thrift                    | 748 us                                                                                                            | 880 us: 1.18x slower                                                                                                    |
| k_core                    | 1.90 sec                                                                                                          | 2.24 sec: 1.18x slower                                                                                                  |
| raytrace                  | 252 ms                                                                                                            | 298 ms: 1.18x slower                                                                                                    |
| django_template           | 33.9 ms                                                                                                           | 40.0 ms: 1.18x slower                                                                                                   |
| scimark_lu                | 110 ms                                                                                                            | 130 ms: 1.18x slower                                                                                                    |
| logging_format            | 6.53 us                                                                                                           | 7.76 us: 1.19x slower                                                                                                   |
| deltablue                 | 3.09 ms                                                                                                           | 3.68 ms: 1.19x slower                                                                                                   |
| meteor_contest            | 99.3 ms                                                                                                           | 119 ms: 1.20x slower                                                                                                    |
| shortest_path             | 445 ms                                                                                                            | 537 ms: 1.21x slower                                                                                                    |
| sqlglot_v2_parse          | 1.20 ms                                                                                                           | 1.46 ms: 1.21x slower                                                                                                   |
| connected_components      | 402 ms                                                                                                            | 491 ms: 1.22x slower                                                                                                    |
| bench_mp_pool             | 12.4 ms                                                                                                           | 15.2 ms: 1.23x slower                                                                                                   |
| richards                  | 41.7 ms                                                                                                           | 51.3 ms: 1.23x slower                                                                                                   |
| genshi_xml                | 47.5 ms                                                                                                           | 58.6 ms: 1.23x slower                                                                                                   |
| crypto_pyaes              | 68.6 ms                                                                                                           | 85.0 ms: 1.24x slower                                                                                                   |
| scimark_sparse_mat_mult   | 4.32 ms                                                                                                           | 5.36 ms: 1.24x slower                                                                                                   |
| richards_super            | 47.4 ms                                                                                                           | 58.9 ms: 1.24x slower                                                                                                   |
| scimark_monte_carlo       | 62.1 ms                                                                                                           | 77.8 ms: 1.25x slower                                                                                                   |
| typing_runtime_protocols  | 151 us                                                                                                            | 190 us: 1.26x slower                                                                                                    |
| python_startup            | 12.4 ms                                                                                                           | 15.7 ms: 1.27x slower                                                                                                   |
| genshi_text               | 20.5 ms                                                                                                           | 26.5 ms: 1.29x slower                                                                                                   |
| python_startup_no_site    | 7.22 ms                                                                                                           | 9.58 ms: 1.33x slower                                                                                                   |
| mako                      | 11.6 ms                                                                                                           | 15.5 ms: 1.34x slower                                                                                                   |
| nbody                     | 92.9 ms                                                                                                           | 126 ms: 1.36x slower                                                                                                    |
| coverage                  | 81.2 ms                                                                                                           | 111 ms: 1.36x slower                                                                                                    |
| bench_thread_pool         | 1.00 ms                                                                                                           | 3.06 ms: 3.06x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (4): generators, float, async_tree_cpu_io_mixed_tg, async_tree_memoization

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x