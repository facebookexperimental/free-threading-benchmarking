# Results vs. base

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 473 ms                                                                                                            | 527 ms: 1.11x slower                                                                                                    |
| docutils       | 3.91 sec                                                                                                          | 4.09 sec: 1.05x slower                                                                                                  |
| sphinx         | 1.47 sec                                                                                                          | 1.67 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 952 ms                                                                                                            | 710 ms: 1.34x faster                                                                                                    |
| async_tree_none_tg         | 384 ms                                                                                                            | 319 ms: 1.20x faster                                                                                                    |
| async_tree_io              | 939 ms                                                                                                            | 789 ms: 1.19x faster                                                                                                    |
| async_tree_memoization_tg  | 486 ms                                                                                                            | 431 ms: 1.13x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 693 ms                                                                                                            | 646 ms: 1.07x faster                                                                                                    |
| async_generators           | 525 ms                                                                                                            | 578 ms: 1.10x slower                                                                                                    |
| coroutines                 | 31.5 ms                                                                                                           | 35.2 ms: 1.12x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.06x faster                                                                                                            |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 129 ms                                                                                                            | 159 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 167 ms                                                                                                            | 183 ms: 1.10x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_dna, regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 167 ms                                                                                                            | 144 ms: 1.15x faster                                                                                                    |
| unpickle_pure_python | 290 us                                                                                                            | 302 us: 1.04x slower                                                                                                    |
| json_dumps           | 15.6 ms                                                                                                           | 17.0 ms: 1.09x slower                                                                                                   |
| xml_etree_parse      | 203 ms                                                                                                            | 223 ms: 1.10x slower                                                                                                    |
| xml_etree_generate   | 123 ms                                                                                                            | 140 ms: 1.14x slower                                                                                                    |
| tomli_loads          | 2.52 sec                                                                                                          | 2.87 sec: 1.14x slower                                                                                                  |
| json_loads           | 39.7 us                                                                                                           | 47.4 us: 1.20x slower                                                                                                   |
| xml_etree_process    | 77.0 ms                                                                                                           | 95.0 ms: 1.23x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 31.8 ms                                                                                                           | 40.9 ms: 1.29x slower                                                                                                   |
| python_startup_no_site | 20.3 ms                                                                                                           | 26.2 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 47.1 ms                                                                                                           | 50.5 ms: 1.07x slower                                                                                                   |
| genshi_xml      | 71.6 ms                                                                                                           | 83.9 ms: 1.17x slower                                                                                                   |
| mako            | 18.7 ms                                                                                                           | 25.7 ms: 1.38x slower                                                                                                   |
| genshi_text     | 28.7 ms                                                                                                           | 41.3 ms: 1.44x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.26x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.37 ms                                                                                                           | 4.15 ms: 2.02x faster                                                                                                   |
| create_gc_cycles           | 4.09 ms                                                                                                           | 2.97 ms: 1.38x faster                                                                                                   |
| async_tree_io_tg           | 952 ms                                                                                                            | 710 ms: 1.34x faster                                                                                                    |
| async_tree_none_tg         | 384 ms                                                                                                            | 319 ms: 1.20x faster                                                                                                    |
| async_tree_io              | 939 ms                                                                                                            | 789 ms: 1.19x faster                                                                                                    |
| xml_etree_iterparse        | 167 ms                                                                                                            | 144 ms: 1.15x faster                                                                                                    |
| async_tree_memoization_tg  | 486 ms                                                                                                            | 431 ms: 1.13x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 693 ms                                                                                                            | 646 ms: 1.07x faster                                                                                                    |
| unpickle_pure_python       | 290 us                                                                                                            | 302 us: 1.04x slower                                                                                                    |
| docutils                   | 3.91 sec                                                                                                          | 4.09 sec: 1.05x slower                                                                                                  |
| logging_silent             | 127 ns                                                                                                            | 134 ns: 1.06x slower                                                                                                    |
| deltablue                  | 4.54 ms                                                                                                           | 4.84 ms: 1.07x slower                                                                                                   |
| shortest_path              | 951 ms                                                                                                            | 1.01 sec: 1.07x slower                                                                                                  |
| deepcopy                   | 344 us                                                                                                            | 368 us: 1.07x slower                                                                                                    |
| django_template            | 47.1 ms                                                                                                           | 50.5 ms: 1.07x slower                                                                                                   |
| logging_format             | 10.2 us                                                                                                           | 11.1 us: 1.09x slower                                                                                                   |
| scimark_sor                | 154 ms                                                                                                            | 168 ms: 1.09x slower                                                                                                    |
| subparsers                 | 32.2 ms                                                                                                           | 35.2 ms: 1.09x slower                                                                                                   |
| json_dumps                 | 15.6 ms                                                                                                           | 17.0 ms: 1.09x slower                                                                                                   |
| deepcopy_memo              | 39.0 us                                                                                                           | 42.8 us: 1.10x slower                                                                                                   |
| xml_etree_parse            | 203 ms                                                                                                            | 223 ms: 1.10x slower                                                                                                    |
| regex_compile              | 167 ms                                                                                                            | 183 ms: 1.10x slower                                                                                                    |
| async_generators           | 525 ms                                                                                                            | 578 ms: 1.10x slower                                                                                                    |
| go                         | 153 ms                                                                                                            | 168 ms: 1.10x slower                                                                                                    |
| telco                      | 10.6 ms                                                                                                           | 11.7 ms: 1.11x slower                                                                                                   |
| connected_components       | 861 ms                                                                                                            | 957 ms: 1.11x slower                                                                                                    |
| richards                   | 58.7 ms                                                                                                           | 65.3 ms: 1.11x slower                                                                                                   |
| 2to3                       | 473 ms                                                                                                            | 527 ms: 1.11x slower                                                                                                    |
| pprint_safe_repr           | 920 ms                                                                                                            | 1.03 sec: 1.12x slower                                                                                                  |
| scimark_fft                | 438 ms                                                                                                            | 488 ms: 1.12x slower                                                                                                    |
| nqueens                    | 107 ms                                                                                                            | 119 ms: 1.12x slower                                                                                                    |
| coroutines                 | 31.5 ms                                                                                                           | 35.2 ms: 1.12x slower                                                                                                   |
| logging_simple             | 8.89 us                                                                                                           | 10.0 us: 1.13x slower                                                                                                   |
| pylint                     | 405 ms                                                                                                            | 457 ms: 1.13x slower                                                                                                    |
| sympy_expand               | 610 ms                                                                                                            | 689 ms: 1.13x slower                                                                                                    |
| sphinx                     | 1.47 sec                                                                                                          | 1.67 sec: 1.14x slower                                                                                                  |
| xml_etree_generate         | 123 ms                                                                                                            | 140 ms: 1.14x slower                                                                                                    |
| tomli_loads                | 2.52 sec                                                                                                          | 2.87 sec: 1.14x slower                                                                                                  |
| sqlglot_v2_transpile       | 2.16 ms                                                                                                           | 2.52 ms: 1.17x slower                                                                                                   |
| sqlglot_v2_optimize        | 71.1 ms                                                                                                           | 83.1 ms: 1.17x slower                                                                                                   |
| scimark_lu                 | 148 ms                                                                                                            | 173 ms: 1.17x slower                                                                                                    |
| genshi_xml                 | 71.6 ms                                                                                                           | 83.9 ms: 1.17x slower                                                                                                   |
| spectral_norm              | 126 ms                                                                                                            | 148 ms: 1.17x slower                                                                                                    |
| pprint_pformat             | 1.87 sec                                                                                                          | 2.21 sec: 1.18x slower                                                                                                  |
| json_loads                 | 39.7 us                                                                                                           | 47.4 us: 1.20x slower                                                                                                   |
| richards_super             | 63.5 ms                                                                                                           | 76.2 ms: 1.20x slower                                                                                                   |
| raytrace                   | 335 ms                                                                                                            | 403 ms: 1.20x slower                                                                                                    |
| typing_runtime_protocols   | 214 us                                                                                                            | 259 us: 1.21x slower                                                                                                    |
| many_optionals             | 1.25 ms                                                                                                           | 1.51 ms: 1.21x slower                                                                                                   |
| deepcopy_reduce            | 3.54 us                                                                                                           | 4.30 us: 1.22x slower                                                                                                   |
| pyflate                    | 606 ms                                                                                                            | 737 ms: 1.22x slower                                                                                                    |
| chaos                      | 74.4 ms                                                                                                           | 91.0 ms: 1.22x slower                                                                                                   |
| hexiom                     | 8.04 ms                                                                                                           | 9.86 ms: 1.23x slower                                                                                                   |
| xml_etree_process          | 77.0 ms                                                                                                           | 95.0 ms: 1.23x slower                                                                                                   |
| nbody                      | 129 ms                                                                                                            | 159 ms: 1.24x slower                                                                                                    |
| mdp                        | 1.98 sec                                                                                                          | 2.46 sec: 1.24x slower                                                                                                  |
| bpe_tokeniser              | 6.12 sec                                                                                                          | 7.61 sec: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 84.5 ms                                                                                                           | 105 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 27.7 ms                                                                                                           | 34.6 ms: 1.25x slower                                                                                                   |
| sympy_sum                  | 198 ms                                                                                                            | 248 ms: 1.26x slower                                                                                                    |
| fannkuch                   | 505 ms                                                                                                            | 636 ms: 1.26x slower                                                                                                    |
| sqlalchemy_declarative     | 181 ms                                                                                                            | 229 ms: 1.27x slower                                                                                                    |
| python_startup             | 31.8 ms                                                                                                           | 40.9 ms: 1.29x slower                                                                                                   |
| python_startup_no_site     | 20.3 ms                                                                                                           | 26.2 ms: 1.29x slower                                                                                                   |
| sympy_str                  | 361 ms                                                                                                            | 466 ms: 1.29x slower                                                                                                    |
| meteor_contest             | 142 ms                                                                                                            | 185 ms: 1.30x slower                                                                                                    |
| comprehensions             | 21.9 us                                                                                                           | 29.1 us: 1.33x slower                                                                                                   |
| sqlglot_v2_parse           | 1.60 ms                                                                                                           | 2.14 ms: 1.34x slower                                                                                                   |
| scimark_sparse_mat_mult    | 5.75 ms                                                                                                           | 7.70 ms: 1.34x slower                                                                                                   |
| bench_thread_pool          | 3.88 ms                                                                                                           | 5.34 ms: 1.38x slower                                                                                                   |
| mako                       | 18.7 ms                                                                                                           | 25.7 ms: 1.38x slower                                                                                                   |
| dulwich_log                | 83.0 ms                                                                                                           | 116 ms: 1.40x slower                                                                                                    |
| coverage                   | 112 ms                                                                                                            | 158 ms: 1.41x slower                                                                                                    |
| genshi_text                | 28.7 ms                                                                                                           | 41.3 ms: 1.44x slower                                                                                                   |
| crypto_pyaes               | 93.0 ms                                                                                                           | 138 ms: 1.49x slower                                                                                                    |
| sqlalchemy_imperative      | 22.3 ms                                                                                                           | 33.9 ms: 1.52x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (18): sqlite_synth, async_tree_cpu_io_mixed, pycparser, pickle_pure_python, float, bench_mp_pool, async_tree_none, async_tree_memoization, regex_dna, regex_effbot, asyncio_websockets, pathlib, k_core, regex_v8, generators, sqlglot_v2_normalize, json, pidigits
Ignored benchmarks (1) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: html5lib

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.19x