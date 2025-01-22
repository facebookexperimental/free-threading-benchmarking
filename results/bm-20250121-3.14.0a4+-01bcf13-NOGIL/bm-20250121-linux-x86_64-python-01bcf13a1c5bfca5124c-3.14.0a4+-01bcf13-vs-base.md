# Results vs. base

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.128x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 510 ms                                                                                                            | 567 ms: 1.11x slower                                                                                                    |
| docutils       | 3.61 sec                                                                                                          | 4.15 sec: 1.15x slower                                                                                                  |
| html5lib       | 90.3 ms                                                                                                           | 115 ms: 1.28x slower                                                                                                    |
| sphinx         | 1.53 sec                                                                                                          | 1.79 sec: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 886 ms                                                                                                            | 830 ms: 1.07x faster                                                                                                    |
| asyncio_websockets         | 766 ms                                                                                                            | 807 ms: 1.05x slower                                                                                                    |
| async_generators           | 543 ms                                                                                                            | 587 ms: 1.08x slower                                                                                                    |
| async_tree_none            | 400 ms                                                                                                            | 438 ms: 1.09x slower                                                                                                    |
| async_tree_io              | 892 ms                                                                                                            | 988 ms: 1.11x slower                                                                                                    |
| coroutines                 | 33.3 ms                                                                                                           | 37.4 ms: 1.12x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 696 ms                                                                                                            | 786 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 745 ms                                                                                                            | 845 ms: 1.13x slower                                                                                                    |
| async_tree_memoization     | 504 ms                                                                                                            | 587 ms: 1.16x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 275 ms                                                                                                            | 241 ms: 1.14x faster                                                                                                    |
| float          | 115 ms                                                                                                            | 105 ms: 1.09x faster                                                                                                    |
| nbody          | 141 ms                                                                                                            | 206 ms: 1.46x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 36.1 ms                                                                                                           | 33.1 ms: 1.09x faster                                                                                                   |
| regex_dna      | 279 ms                                                                                                            | 300 ms: 1.07x slower                                                                                                    |
| regex_compile  | 193 ms                                                                                                            | 222 ms: 1.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_dumps           | 19.9 ms                                                                                                           | 16.4 ms: 1.21x faster                                                                                                   |
| xml_etree_iterparse  | 167 ms                                                                                                            | 152 ms: 1.10x faster                                                                                                    |
| xml_etree_parse      | 209 ms                                                                                                            | 236 ms: 1.13x slower                                                                                                    |
| tomli_loads          | 2.68 sec                                                                                                          | 3.22 sec: 1.20x slower                                                                                                  |
| xml_etree_generate   | 136 ms                                                                                                            | 167 ms: 1.23x slower                                                                                                    |
| xml_etree_process    | 85.6 ms                                                                                                           | 110 ms: 1.28x slower                                                                                                    |
| unpickle_pure_python | 304 us                                                                                                            | 392 us: 1.29x slower                                                                                                    |
| pickle_pure_python   | 469 us                                                                                                            | 668 us: 1.43x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 30.8 ms                                                                                                           | 34.9 ms: 1.13x slower                                                                                                   |
| python_startup_no_site | 18.0 ms                                                                                                           | 21.3 ms: 1.18x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 51.0 ms                                                                                                           | 55.1 ms: 1.08x slower                                                                                                   |
| mako            | 18.1 ms                                                                                                           | 22.8 ms: 1.26x slower                                                                                                   |
| genshi_xml      | 77.9 ms                                                                                                           | 104 ms: 1.34x slower                                                                                                    |
| genshi_text     | 30.6 ms                                                                                                           | 43.2 ms: 1.41x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.27x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json | results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 4.11 ms                                                                                                           | 2.95 ms: 1.39x faster                                                                                                   |
| json_dumps                 | 19.9 ms                                                                                                           | 16.4 ms: 1.21x faster                                                                                                   |
| pidigits                   | 275 ms                                                                                                            | 241 ms: 1.14x faster                                                                                                    |
| xml_etree_iterparse        | 167 ms                                                                                                            | 152 ms: 1.10x faster                                                                                                    |
| regex_v8                   | 36.1 ms                                                                                                           | 33.1 ms: 1.09x faster                                                                                                   |
| float                      | 115 ms                                                                                                            | 105 ms: 1.09x faster                                                                                                    |
| bench_mp_pool              | 98.9 ms                                                                                                           | 92.5 ms: 1.07x faster                                                                                                   |
| async_tree_io_tg           | 886 ms                                                                                                            | 830 ms: 1.07x faster                                                                                                    |
| asyncio_websockets         | 766 ms                                                                                                            | 807 ms: 1.05x slower                                                                                                    |
| k_core                     | 4.29 sec                                                                                                          | 4.57 sec: 1.07x slower                                                                                                  |
| sqlglot_normalize          | 158 ms                                                                                                            | 169 ms: 1.07x slower                                                                                                    |
| regex_dna                  | 279 ms                                                                                                            | 300 ms: 1.07x slower                                                                                                    |
| json                       | 7.18 ms                                                                                                           | 7.74 ms: 1.08x slower                                                                                                   |
| django_template            | 51.0 ms                                                                                                           | 55.1 ms: 1.08x slower                                                                                                   |
| async_generators           | 543 ms                                                                                                            | 587 ms: 1.08x slower                                                                                                    |
| spectral_norm              | 147 ms                                                                                                            | 160 ms: 1.09x slower                                                                                                    |
| subparsers                 | 38.3 ms                                                                                                           | 41.7 ms: 1.09x slower                                                                                                   |
| async_tree_none            | 400 ms                                                                                                            | 438 ms: 1.09x slower                                                                                                    |
| shortest_path              | 943 ms                                                                                                            | 1.04 sec: 1.10x slower                                                                                                  |
| async_tree_io              | 892 ms                                                                                                            | 988 ms: 1.11x slower                                                                                                    |
| richards                   | 65.0 ms                                                                                                           | 72.1 ms: 1.11x slower                                                                                                   |
| 2to3                       | 510 ms                                                                                                            | 567 ms: 1.11x slower                                                                                                    |
| fannkuch                   | 592 ms                                                                                                            | 659 ms: 1.11x slower                                                                                                    |
| connected_components       | 852 ms                                                                                                            | 949 ms: 1.11x slower                                                                                                    |
| logging_simple             | 9.54 us                                                                                                           | 10.6 us: 1.12x slower                                                                                                   |
| coroutines                 | 33.3 ms                                                                                                           | 37.4 ms: 1.12x slower                                                                                                   |
| dulwich_log                | 110 ms                                                                                                            | 123 ms: 1.12x slower                                                                                                    |
| richards_super             | 75.2 ms                                                                                                           | 84.5 ms: 1.12x slower                                                                                                   |
| sympy_integrate            | 32.1 ms                                                                                                           | 36.1 ms: 1.12x slower                                                                                                   |
| xml_etree_parse            | 209 ms                                                                                                            | 236 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 696 ms                                                                                                            | 786 ms: 1.13x slower                                                                                                    |
| python_startup             | 30.8 ms                                                                                                           | 34.9 ms: 1.13x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 745 ms                                                                                                            | 845 ms: 1.13x slower                                                                                                    |
| sqlglot_optimize           | 78.6 ms                                                                                                           | 89.5 ms: 1.14x slower                                                                                                   |
| telco                      | 11.9 ms                                                                                                           | 13.6 ms: 1.14x slower                                                                                                   |
| regex_compile              | 193 ms                                                                                                            | 222 ms: 1.15x slower                                                                                                    |
| docutils                   | 3.61 sec                                                                                                          | 4.15 sec: 1.15x slower                                                                                                  |
| scimark_sor                | 157 ms                                                                                                            | 181 ms: 1.16x slower                                                                                                    |
| generators                 | 42.7 ms                                                                                                           | 49.6 ms: 1.16x slower                                                                                                   |
| async_tree_memoization     | 504 ms                                                                                                            | 587 ms: 1.16x slower                                                                                                    |
| sphinx                     | 1.53 sec                                                                                                          | 1.79 sec: 1.16x slower                                                                                                  |
| pylint                     | 414 ms                                                                                                            | 483 ms: 1.17x slower                                                                                                    |
| crypto_pyaes               | 110 ms                                                                                                            | 129 ms: 1.17x slower                                                                                                    |
| mdp                        | 3.55 sec                                                                                                          | 4.19 sec: 1.18x slower                                                                                                  |
| python_startup_no_site     | 18.0 ms                                                                                                           | 21.3 ms: 1.18x slower                                                                                                   |
| sympy_expand               | 580 ms                                                                                                            | 686 ms: 1.18x slower                                                                                                    |
| hexiom                     | 9.28 ms                                                                                                           | 11.0 ms: 1.19x slower                                                                                                   |
| tomli_loads                | 2.68 sec                                                                                                          | 3.22 sec: 1.20x slower                                                                                                  |
| nqueens                    | 113 ms                                                                                                            | 137 ms: 1.21x slower                                                                                                    |
| scimark_sparse_mat_mult    | 7.52 ms                                                                                                           | 9.10 ms: 1.21x slower                                                                                                   |
| sqlalchemy_declarative     | 189 ms                                                                                                            | 231 ms: 1.22x slower                                                                                                    |
| pprint_safe_repr           | 961 ms                                                                                                            | 1.18 sec: 1.23x slower                                                                                                  |
| xml_etree_generate         | 136 ms                                                                                                            | 167 ms: 1.23x slower                                                                                                    |
| pprint_pformat             | 1.96 sec                                                                                                          | 2.44 sec: 1.24x slower                                                                                                  |
| meteor_contest             | 148 ms                                                                                                            | 185 ms: 1.25x slower                                                                                                    |
| sqlglot_transpile          | 2.38 ms                                                                                                           | 2.98 ms: 1.25x slower                                                                                                   |
| sympy_str                  | 382 ms                                                                                                            | 480 ms: 1.26x slower                                                                                                    |
| mako                       | 18.1 ms                                                                                                           | 22.8 ms: 1.26x slower                                                                                                   |
| scimark_fft                | 453 ms                                                                                                            | 578 ms: 1.28x slower                                                                                                    |
| html5lib                   | 90.3 ms                                                                                                           | 115 ms: 1.28x slower                                                                                                    |
| xml_etree_process          | 85.6 ms                                                                                                           | 110 ms: 1.28x slower                                                                                                    |
| coverage                   | 120 ms                                                                                                            | 155 ms: 1.29x slower                                                                                                    |
| unpickle_pure_python       | 304 us                                                                                                            | 392 us: 1.29x slower                                                                                                    |
| bpe_tokeniser              | 5.96 sec                                                                                                          | 7.77 sec: 1.30x slower                                                                                                  |
| raytrace                   | 349 ms                                                                                                            | 463 ms: 1.33x slower                                                                                                    |
| go                         | 171 ms                                                                                                            | 227 ms: 1.33x slower                                                                                                    |
| deepcopy_memo              | 40.3 us                                                                                                           | 53.6 us: 1.33x slower                                                                                                   |
| genshi_xml                 | 77.9 ms                                                                                                           | 104 ms: 1.34x slower                                                                                                    |
| pyflate                    | 675 ms                                                                                                            | 906 ms: 1.34x slower                                                                                                    |
| scimark_monte_carlo        | 88.3 ms                                                                                                           | 119 ms: 1.35x slower                                                                                                    |
| deepcopy                   | 394 us                                                                                                            | 533 us: 1.35x slower                                                                                                    |
| scimark_lu                 | 152 ms                                                                                                            | 206 ms: 1.36x slower                                                                                                    |
| deepcopy_reduce            | 3.46 us                                                                                                           | 4.70 us: 1.36x slower                                                                                                   |
| sqlglot_parse              | 1.85 ms                                                                                                           | 2.55 ms: 1.38x slower                                                                                                   |
| chaos                      | 78.6 ms                                                                                                           | 110 ms: 1.40x slower                                                                                                    |
| thrift                     | 1.06 ms                                                                                                           | 1.48 ms: 1.40x slower                                                                                                   |
| genshi_text                | 30.6 ms                                                                                                           | 43.2 ms: 1.41x slower                                                                                                   |
| sqlalchemy_imperative      | 24.5 ms                                                                                                           | 34.6 ms: 1.41x slower                                                                                                   |
| pickle_pure_python         | 469 us                                                                                                            | 668 us: 1.43x slower                                                                                                    |
| comprehensions             | 20.3 us                                                                                                           | 29.5 us: 1.46x slower                                                                                                   |
| sympy_sum                  | 198 ms                                                                                                            | 288 ms: 1.46x slower                                                                                                    |
| nbody                      | 141 ms                                                                                                            | 206 ms: 1.46x slower                                                                                                    |
| deltablue                  | 4.68 ms                                                                                                           | 7.05 ms: 1.51x slower                                                                                                   |
| typing_runtime_protocols   | 208 us                                                                                                            | 327 us: 1.57x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (12): gc_traversal, regex_effbot, pycparser, json_loads, async_tree_memoization_tg, bench_thread_pool, sqlite_synth, pathlib, logging_silent, async_tree_none_tg, many_optionals, logging_format

- Geometric mean (including insignificant results): 1.128x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x