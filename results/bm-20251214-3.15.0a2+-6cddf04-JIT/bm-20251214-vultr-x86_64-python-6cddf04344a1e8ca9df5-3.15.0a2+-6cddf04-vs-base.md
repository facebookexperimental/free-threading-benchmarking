# Results vs. base

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.039x faster
- HPT reliability: 98.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 244 ms                                                                                                            | 247 ms: 1.01x slower                                                                                                  |
| html5lib       | 59.2 ms                                                                                                           | 66.9 ms: 1.13x slower                                                                                                 |
| sphinx         | 965 ms                                                                                                            | 1000 ms: 1.04x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 521 ms                                                                                                            | 480 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 522 ms                                                                                                            | 485 ms: 1.08x faster                                                                                                  |
| asyncio_tcp                | 450 ms                                                                                                            | 442 ms: 1.02x faster                                                                                                  |
| async_tree_memoization_tg  | 303 ms                                                                                                            | 305 ms: 1.01x slower                                                                                                  |
| coroutines                 | 23.5 ms                                                                                                           | 23.7 ms: 1.01x slower                                                                                                 |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                          | 1.47 sec: 1.01x slower                                                                                                |
| async_tree_io_tg           | 581 ms                                                                                                            | 590 ms: 1.01x slower                                                                                                  |
| async_generators           | 343 ms                                                                                                            | 358 ms: 1.04x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (5): async_tree_memoization, asyncio_websockets, async_tree_none_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 90.0 ms                                                                                                           | 71.5 ms: 1.26x faster                                                                                                 |
| float          | 69.8 ms                                                                                                           | 58.9 ms: 1.18x faster                                                                                                 |
| pidigits       | 215 ms                                                                                                            | 195 ms: 1.10x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 177 ms                                                                                                            | 167 ms: 1.06x faster                                                                                                  |
| regex_effbot   | 2.85 ms                                                                                                           | 2.71 ms: 1.05x faster                                                                                                 |
| regex_v8       | 22.4 ms                                                                                                           | 22.0 ms: 1.02x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 211 us                                                                                                            | 182 us: 1.16x faster                                                                                                  |
| tomli_loads          | 2.15 sec                                                                                                          | 1.98 sec: 1.09x faster                                                                                                |
| xml_etree_process    | 57.5 ms                                                                                                           | 53.6 ms: 1.07x faster                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                            | 288 us: 1.06x faster                                                                                                  |
| xml_etree_generate   | 82.0 ms                                                                                                           | 77.3 ms: 1.06x faster                                                                                                 |
| json_dumps           | 9.84 ms                                                                                                           | 9.41 ms: 1.05x faster                                                                                                 |
| pickle_list          | 5.28 us                                                                                                           | 5.06 us: 1.04x faster                                                                                                 |
| pickle_dict          | 32.5 us                                                                                                           | 31.6 us: 1.03x faster                                                                                                 |
| pickle               | 12.7 us                                                                                                           | 12.4 us: 1.03x faster                                                                                                 |
| unpickle_list        | 5.20 us                                                                                                           | 5.14 us: 1.01x faster                                                                                                 |
| json_loads           | 27.5 us                                                                                                           | 27.6 us: 1.01x slower                                                                                                 |
| unpickle             | 14.1 us                                                                                                           | 14.5 us: 1.03x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                                                           | 7.32 ms: 1.01x slower                                                                                                 |
| python_startup         | 12.3 ms                                                                                                           | 12.6 ms: 1.02x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 11.5 ms                                                                                                           | 10.6 ms: 1.09x faster                                                                                                 |
| django_template | 35.6 ms                                                                                                           | 34.8 ms: 1.02x faster                                                                                                 |
| genshi_text     | 20.9 ms                                                                                                           | 21.2 ms: 1.01x slower                                                                                                 |
| genshi_xml      | 49.2 ms                                                                                                           | 53.0 ms: 1.08x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.01x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json | results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                   | 42.1 ms                                                                                                           | 19.7 ms: 2.14x faster                                                                                                 |
| richards_super             | 47.8 ms                                                                                                           | 23.8 ms: 2.01x faster                                                                                                 |
| bench_mp_pool              | 329 ms                                                                                                            | 238 ms: 1.38x faster                                                                                                  |
| nbody                      | 90.0 ms                                                                                                           | 71.5 ms: 1.26x faster                                                                                                 |
| deltablue                  | 3.31 ms                                                                                                           | 2.73 ms: 1.21x faster                                                                                                 |
| scimark_fft                | 300 ms                                                                                                            | 249 ms: 1.20x faster                                                                                                  |
| float                      | 69.8 ms                                                                                                           | 58.9 ms: 1.18x faster                                                                                                 |
| logging_silent             | 101 ns                                                                                                            | 86.1 ns: 1.17x faster                                                                                                 |
| unpickle_pure_python       | 211 us                                                                                                            | 182 us: 1.16x faster                                                                                                  |
| scimark_monte_carlo        | 62.9 ms                                                                                                           | 54.6 ms: 1.15x faster                                                                                                 |
| pyflate                    | 413 ms                                                                                                            | 371 ms: 1.11x faster                                                                                                  |
| pidigits                   | 215 ms                                                                                                            | 195 ms: 1.10x faster                                                                                                  |
| spectral_norm              | 93.9 ms                                                                                                           | 85.3 ms: 1.10x faster                                                                                                 |
| scimark_sor                | 107 ms                                                                                                            | 97.7 ms: 1.10x faster                                                                                                 |
| mako                       | 11.5 ms                                                                                                           | 10.6 ms: 1.09x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 521 ms                                                                                                            | 480 ms: 1.09x faster                                                                                                  |
| tomli_loads                | 2.15 sec                                                                                                          | 1.98 sec: 1.09x faster                                                                                                |
| deepcopy_memo              | 26.3 us                                                                                                           | 24.3 us: 1.08x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 522 ms                                                                                                            | 485 ms: 1.08x faster                                                                                                  |
| xml_etree_process          | 57.5 ms                                                                                                           | 53.6 ms: 1.07x faster                                                                                                 |
| pprint_safe_repr           | 685 ms                                                                                                            | 639 ms: 1.07x faster                                                                                                  |
| fannkuch                   | 388 ms                                                                                                            | 363 ms: 1.07x faster                                                                                                  |
| pickle_pure_python         | 306 us                                                                                                            | 288 us: 1.06x faster                                                                                                  |
| sqlite_synth               | 2.33 us                                                                                                           | 2.20 us: 1.06x faster                                                                                                 |
| xml_etree_generate         | 82.0 ms                                                                                                           | 77.3 ms: 1.06x faster                                                                                                 |
| regex_dna                  | 177 ms                                                                                                            | 167 ms: 1.06x faster                                                                                                  |
| pprint_pformat             | 1.40 sec                                                                                                          | 1.33 sec: 1.06x faster                                                                                                |
| go                         | 106 ms                                                                                                            | 100 ms: 1.05x faster                                                                                                  |
| regex_effbot               | 2.85 ms                                                                                                           | 2.71 ms: 1.05x faster                                                                                                 |
| json_dumps                 | 9.84 ms                                                                                                           | 9.41 ms: 1.05x faster                                                                                                 |
| pickle_list                | 5.28 us                                                                                                           | 5.06 us: 1.04x faster                                                                                                 |
| bpe_tokeniser              | 4.18 sec                                                                                                          | 4.01 sec: 1.04x faster                                                                                                |
| crypto_pyaes               | 68.7 ms                                                                                                           | 66.1 ms: 1.04x faster                                                                                                 |
| chaos                      | 55.1 ms                                                                                                           | 53.2 ms: 1.03x faster                                                                                                 |
| meteor_contest             | 101 ms                                                                                                            | 97.9 ms: 1.03x faster                                                                                                 |
| scimark_lu                 | 107 ms                                                                                                            | 103 ms: 1.03x faster                                                                                                  |
| thrift                     | 758 us                                                                                                            | 735 us: 1.03x faster                                                                                                  |
| json                       | 5.04 ms                                                                                                           | 4.89 ms: 1.03x faster                                                                                                 |
| pickle_dict                | 32.5 us                                                                                                           | 31.6 us: 1.03x faster                                                                                                 |
| pickle                     | 12.7 us                                                                                                           | 12.4 us: 1.03x faster                                                                                                 |
| deepcopy_reduce            | 2.56 us                                                                                                           | 2.50 us: 1.03x faster                                                                                                 |
| django_template            | 35.6 ms                                                                                                           | 34.8 ms: 1.02x faster                                                                                                 |
| scimark_sparse_mat_mult    | 4.35 ms                                                                                                           | 4.25 ms: 1.02x faster                                                                                                 |
| k_core                     | 1.86 sec                                                                                                          | 1.82 sec: 1.02x faster                                                                                                |
| connected_components       | 384 ms                                                                                                            | 376 ms: 1.02x faster                                                                                                  |
| regex_v8                   | 22.4 ms                                                                                                           | 22.0 ms: 1.02x faster                                                                                                 |
| asyncio_tcp                | 450 ms                                                                                                            | 442 ms: 1.02x faster                                                                                                  |
| pycparser                  | 1.11 sec                                                                                                          | 1.09 sec: 1.01x faster                                                                                                |
| unpickle_list              | 5.20 us                                                                                                           | 5.14 us: 1.01x faster                                                                                                 |
| coverage                   | 82.0 ms                                                                                                           | 81.2 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_parse           | 1.19 ms                                                                                                           | 1.18 ms: 1.01x faster                                                                                                 |
| shortest_path              | 429 ms                                                                                                            | 429 ms: 1.00x slower                                                                                                  |
| pathlib                    | 17.4 ms                                                                                                           | 17.5 ms: 1.01x slower                                                                                                 |
| json_loads                 | 27.5 us                                                                                                           | 27.6 us: 1.01x slower                                                                                                 |
| async_tree_memoization_tg  | 303 ms                                                                                                            | 305 ms: 1.01x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                           | 1.50 ms: 1.01x slower                                                                                                 |
| coroutines                 | 23.5 ms                                                                                                           | 23.7 ms: 1.01x slower                                                                                                 |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.86 ms: 1.01x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                           | 7.32 ms: 1.01x slower                                                                                                 |
| 2to3                       | 244 ms                                                                                                            | 247 ms: 1.01x slower                                                                                                  |
| gc_traversal               | 4.43 ms                                                                                                           | 4.48 ms: 1.01x slower                                                                                                 |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                          | 1.47 sec: 1.01x slower                                                                                                |
| genshi_text                | 20.9 ms                                                                                                           | 21.2 ms: 1.01x slower                                                                                                 |
| async_tree_io_tg           | 581 ms                                                                                                            | 590 ms: 1.01x slower                                                                                                  |
| telco                      | 159 ms                                                                                                            | 162 ms: 1.02x slower                                                                                                  |
| subparsers                 | 9.11 ms                                                                                                           | 9.26 ms: 1.02x slower                                                                                                 |
| python_startup             | 12.3 ms                                                                                                           | 12.6 ms: 1.02x slower                                                                                                 |
| typing_runtime_protocols   | 152 us                                                                                                            | 156 us: 1.03x slower                                                                                                  |
| generators                 | 27.4 ms                                                                                                           | 28.1 ms: 1.03x slower                                                                                                 |
| comprehensions             | 15.8 us                                                                                                           | 16.2 us: 1.03x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                            | 260 ms: 1.03x slower                                                                                                  |
| unpickle                   | 14.1 us                                                                                                           | 14.5 us: 1.03x slower                                                                                                 |
| sphinx                     | 965 ms                                                                                                            | 1000 ms: 1.04x slower                                                                                                 |
| many_optionals             | 945 us                                                                                                            | 984 us: 1.04x slower                                                                                                  |
| async_generators           | 343 ms                                                                                                            | 358 ms: 1.04x slower                                                                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 108 ms: 1.06x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.7 ms                                                                                                           | 54.0 ms: 1.06x slower                                                                                                 |
| dulwich_log                | 68.1 ms                                                                                                           | 73.0 ms: 1.07x slower                                                                                                 |
| genshi_xml                 | 49.2 ms                                                                                                           | 53.0 ms: 1.08x slower                                                                                                 |
| pylint                     | 281 ms                                                                                                            | 305 ms: 1.09x slower                                                                                                  |
| nqueens                    | 78.8 ms                                                                                                           | 85.9 ms: 1.09x slower                                                                                                 |
| hexiom                     | 5.55 ms                                                                                                           | 6.08 ms: 1.10x slower                                                                                                 |
| html5lib                   | 59.2 ms                                                                                                           | 66.9 ms: 1.13x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                          | 1.34 sec: 1.17x slower                                                                                                |
| unpack_sequence            | 41.5 ns                                                                                                           | 81.2 ns: 1.96x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (12): xml_etree_parse, logging_simple, async_tree_memoization, regex_compile, deepcopy, asyncio_websockets, xml_etree_iterparse, async_tree_none_tg, bench_thread_pool, async_tree_none, logging_format, async_tree_io
Ignored benchmarks (5) of results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: docutils, sympy_expand, sympy_integrate, sympy_str, sympy_sum

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 98.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x