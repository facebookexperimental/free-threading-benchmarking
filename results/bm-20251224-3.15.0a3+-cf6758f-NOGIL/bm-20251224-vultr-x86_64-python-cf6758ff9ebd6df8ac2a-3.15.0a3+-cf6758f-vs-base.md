# Results vs. base

- fork: python
- ref: cf6758ff9ebd6df8ac2a
- machine: linux-x86_64
- commit hash: cf6758f
- commit date: 2025-12-24
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 245 ms                                                                                                            | 276 ms: 1.12x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.74 sec: 1.08x slower                                                                                                  |
| html5lib       | 59.5 ms                                                                                                           | 65.8 ms: 1.11x slower                                                                                                   |
| sphinx         | 965 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 543 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| coroutines                 | 23.3 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| async_tree_io_tg           | 584 ms                                                                                                            | 600 ms: 1.03x slower                                                                                                    |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 321 ms: 1.05x slower                                                                                                    |
| async_tree_none_tg         | 243 ms                                                                                                            | 260 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                                                            | 520 ms: 1.07x slower                                                                                                    |
| async_tree_io              | 547 ms                                                                                                            | 606 ms: 1.11x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 486 ms                                                                                                            | 542 ms: 1.12x slower                                                                                                    |
| async_generators           | 337 ms                                                                                                            | 377 ms: 1.12x slower                                                                                                    |
| async_tree_memoization     | 302 ms                                                                                                            | 350 ms: 1.16x slower                                                                                                    |
| async_tree_none            | 241 ms                                                                                                            | 284 ms: 1.18x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 205 ms                                                                                                            | 195 ms: 1.05x faster                                                                                                    |
| float          | 69.7 ms                                                                                                           | 73.9 ms: 1.06x slower                                                                                                   |
| nbody          | 92.5 ms                                                                                                           | 125 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                                                           | 21.0 ms: 1.06x faster                                                                                                   |
| regex_dna      | 178 ms                                                                                                            | 170 ms: 1.05x faster                                                                                                    |
| regex_compile  | 123 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 132 ms: 1.01x slower                                                                                                    |
| xml_etree_iterparse  | 84.6 ms                                                                                                           | 88.4 ms: 1.05x slower                                                                                                   |
| pickle_pure_python   | 306 us                                                                                                            | 332 us: 1.09x slower                                                                                                    |
| tomli_loads          | 2.08 sec                                                                                                          | 2.28 sec: 1.10x slower                                                                                                  |
| json_dumps           | 9.94 ms                                                                                                           | 11.1 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python | 211 us                                                                                                            | 236 us: 1.12x slower                                                                                                    |
| json_loads           | 27.7 us                                                                                                           | 31.5 us: 1.14x slower                                                                                                   |
| xml_etree_generate   | 82.6 ms                                                                                                           | 96.7 ms: 1.17x slower                                                                                                   |
| xml_etree_process    | 57.5 ms                                                                                                           | 69.5 ms: 1.21x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.25 ms                                                                                                           | 9.66 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                                                           | 40.9 ms: 1.17x slower                                                                                                   |
| genshi_xml      | 49.1 ms                                                                                                           | 57.6 ms: 1.17x slower                                                                                                   |
| genshi_text     | 21.1 ms                                                                                                           | 27.0 ms: 1.28x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 15.9 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json | results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 311 ms                                                                                                            | 7.09 ms: 43.85x faster                                                                                                  |
| gc_traversal               | 4.24 ms                                                                                                           | 1.91 ms: 2.21x faster                                                                                                   |
| create_gc_cycles           | 1.88 ms                                                                                                           | 1.48 ms: 1.27x faster                                                                                                   |
| sqlite_synth               | 2.30 us                                                                                                           | 2.06 us: 1.11x faster                                                                                                   |
| asyncio_websockets         | 543 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 22.2 ms                                                                                                           | 21.0 ms: 1.06x faster                                                                                                   |
| pidigits                   | 205 ms                                                                                                            | 195 ms: 1.05x faster                                                                                                    |
| regex_dna                  | 178 ms                                                                                                            | 170 ms: 1.05x faster                                                                                                    |
| logging_silent             | 101 ns                                                                                                            | 100 ns: 1.01x faster                                                                                                    |
| xml_etree_parse            | 130 ms                                                                                                            | 132 ms: 1.01x slower                                                                                                    |
| coroutines                 | 23.3 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| async_tree_io_tg           | 584 ms                                                                                                            | 600 ms: 1.03x slower                                                                                                    |
| dulwich_log                | 66.9 ms                                                                                                           | 69.9 ms: 1.04x slower                                                                                                   |
| pathlib                    | 17.3 ms                                                                                                           | 18.1 ms: 1.04x slower                                                                                                   |
| xml_etree_iterparse        | 84.6 ms                                                                                                           | 88.4 ms: 1.05x slower                                                                                                   |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 321 ms: 1.05x slower                                                                                                    |
| bpe_tokeniser              | 4.17 sec                                                                                                          | 4.39 sec: 1.05x slower                                                                                                  |
| float                      | 69.7 ms                                                                                                           | 73.9 ms: 1.06x slower                                                                                                   |
| many_optionals             | 945 us                                                                                                            | 1.01 ms: 1.07x slower                                                                                                   |
| async_tree_none_tg         | 243 ms                                                                                                            | 260 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                                                            | 520 ms: 1.07x slower                                                                                                    |
| json                       | 4.99 ms                                                                                                           | 5.35 ms: 1.07x slower                                                                                                   |
| pylint                     | 283 ms                                                                                                            | 303 ms: 1.07x slower                                                                                                    |
| deltablue                  | 3.34 ms                                                                                                           | 3.59 ms: 1.07x slower                                                                                                   |
| docutils                   | 2.55 sec                                                                                                          | 2.74 sec: 1.08x slower                                                                                                  |
| sphinx                     | 965 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| sympy_expand               | 481 ms                                                                                                            | 520 ms: 1.08x slower                                                                                                    |
| pickle_pure_python         | 306 us                                                                                                            | 332 us: 1.09x slower                                                                                                    |
| telco                      | 158 ms                                                                                                            | 173 ms: 1.09x slower                                                                                                    |
| tomli_loads                | 2.08 sec                                                                                                          | 2.28 sec: 1.10x slower                                                                                                  |
| html5lib                   | 59.5 ms                                                                                                           | 65.8 ms: 1.11x slower                                                                                                   |
| async_tree_io              | 547 ms                                                                                                            | 606 ms: 1.11x slower                                                                                                    |
| pprint_safe_repr           | 692 ms                                                                                                            | 769 ms: 1.11x slower                                                                                                    |
| sympy_str                  | 276 ms                                                                                                            | 307 ms: 1.11x slower                                                                                                    |
| json_dumps                 | 9.94 ms                                                                                                           | 11.1 ms: 1.11x slower                                                                                                   |
| comprehensions             | 15.9 us                                                                                                           | 17.8 us: 1.12x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 486 ms                                                                                                            | 542 ms: 1.12x slower                                                                                                    |
| bench_thread_pool          | 1.32 ms                                                                                                           | 1.48 ms: 1.12x slower                                                                                                   |
| async_generators           | 337 ms                                                                                                            | 377 ms: 1.12x slower                                                                                                    |
| subparsers                 | 9.10 ms                                                                                                           | 10.2 ms: 1.12x slower                                                                                                   |
| unpickle_pure_python       | 211 us                                                                                                            | 236 us: 1.12x slower                                                                                                    |
| sympy_sum                  | 155 ms                                                                                                            | 174 ms: 1.12x slower                                                                                                    |
| 2to3                       | 245 ms                                                                                                            | 276 ms: 1.12x slower                                                                                                    |
| pprint_pformat             | 1.42 sec                                                                                                          | 1.59 sec: 1.12x slower                                                                                                  |
| go                         | 105 ms                                                                                                            | 119 ms: 1.13x slower                                                                                                    |
| sympy_integrate            | 19.1 ms                                                                                                           | 21.6 ms: 1.13x slower                                                                                                   |
| chaos                      | 56.1 ms                                                                                                           | 63.5 ms: 1.13x slower                                                                                                   |
| nqueens                    | 78.2 ms                                                                                                           | 88.9 ms: 1.14x slower                                                                                                   |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.14x slower                                                                                                  |
| scimark_fft                | 307 ms                                                                                                            | 349 ms: 1.14x slower                                                                                                    |
| deepcopy_memo              | 26.6 us                                                                                                           | 30.2 us: 1.14x slower                                                                                                   |
| json_loads                 | 27.7 us                                                                                                           | 31.5 us: 1.14x slower                                                                                                   |
| scimark_sor                | 106 ms                                                                                                            | 121 ms: 1.14x slower                                                                                                    |
| regex_compile              | 123 ms                                                                                                            | 141 ms: 1.14x slower                                                                                                    |
| pyflate                    | 407 ms                                                                                                            | 466 ms: 1.15x slower                                                                                                    |
| deepcopy                   | 239 us                                                                                                            | 274 us: 1.15x slower                                                                                                    |
| thrift                     | 761 us                                                                                                            | 881 us: 1.16x slower                                                                                                    |
| async_tree_memoization     | 302 ms                                                                                                            | 350 ms: 1.16x slower                                                                                                    |
| raytrace                   | 255 ms                                                                                                            | 296 ms: 1.16x slower                                                                                                    |
| hexiom                     | 5.55 ms                                                                                                           | 6.46 ms: 1.16x slower                                                                                                   |
| django_template            | 35.1 ms                                                                                                           | 40.9 ms: 1.17x slower                                                                                                   |
| sqlglot_v2_optimize        | 50.6 ms                                                                                                           | 59.2 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 82.6 ms                                                                                                           | 96.7 ms: 1.17x slower                                                                                                   |
| genshi_xml                 | 49.1 ms                                                                                                           | 57.6 ms: 1.17x slower                                                                                                   |
| deepcopy_reduce            | 2.52 us                                                                                                           | 2.96 us: 1.17x slower                                                                                                   |
| logging_simple             | 5.81 us                                                                                                           | 6.85 us: 1.18x slower                                                                                                   |
| async_tree_none            | 241 ms                                                                                                            | 284 ms: 1.18x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.48 ms                                                                                                           | 1.76 ms: 1.19x slower                                                                                                   |
| logging_format             | 6.61 us                                                                                                           | 7.85 us: 1.19x slower                                                                                                   |
| meteor_contest             | 102 ms                                                                                                            | 121 ms: 1.19x slower                                                                                                    |
| k_core                     | 1.87 sec                                                                                                          | 2.23 sec: 1.19x slower                                                                                                  |
| fannkuch                   | 386 ms                                                                                                            | 463 ms: 1.20x slower                                                                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                                                            | 121 ms: 1.20x slower                                                                                                    |
| scimark_lu                 | 107 ms                                                                                                            | 129 ms: 1.20x slower                                                                                                    |
| xml_etree_process          | 57.5 ms                                                                                                           | 69.5 ms: 1.21x slower                                                                                                   |
| sqlglot_v2_parse           | 1.18 ms                                                                                                           | 1.43 ms: 1.21x slower                                                                                                   |
| richards                   | 42.3 ms                                                                                                           | 52.2 ms: 1.23x slower                                                                                                   |
| generators                 | 27.6 ms                                                                                                           | 34.0 ms: 1.23x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.35 ms                                                                                                           | 5.36 ms: 1.23x slower                                                                                                   |
| shortest_path              | 431 ms                                                                                                            | 533 ms: 1.24x slower                                                                                                    |
| richards_super             | 48.5 ms                                                                                                           | 60.1 ms: 1.24x slower                                                                                                   |
| spectral_norm              | 92.4 ms                                                                                                           | 115 ms: 1.24x slower                                                                                                    |
| typing_runtime_protocols   | 154 us                                                                                                            | 192 us: 1.25x slower                                                                                                    |
| connected_components       | 388 ms                                                                                                            | 485 ms: 1.25x slower                                                                                                    |
| python_startup             | 12.4 ms                                                                                                           | 15.8 ms: 1.27x slower                                                                                                   |
| crypto_pyaes               | 68.4 ms                                                                                                           | 87.2 ms: 1.27x slower                                                                                                   |
| scimark_monte_carlo        | 61.7 ms                                                                                                           | 78.8 ms: 1.28x slower                                                                                                   |
| genshi_text                | 21.1 ms                                                                                                           | 27.0 ms: 1.28x slower                                                                                                   |
| mako                       | 12.1 ms                                                                                                           | 15.9 ms: 1.32x slower                                                                                                   |
| python_startup_no_site     | 7.25 ms                                                                                                           | 9.66 ms: 1.33x slower                                                                                                   |
| nbody                      | 92.5 ms                                                                                                           | 125 ms: 1.36x slower                                                                                                    |
| coverage                   | 81.2 ms                                                                                                           | 112 ms: 1.38x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, pycparser

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x