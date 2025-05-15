# Results vs. base

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 339 ms                                                                                                          | 378 ms: 1.11x slower                                                                                                  |
| docutils       | 3.39 sec                                                                                                        | 3.61 sec: 1.06x slower                                                                                                |
| html5lib       | 75.2 ms                                                                                                         | 82.8 ms: 1.10x slower                                                                                                 |
| sphinx         | 1.29 sec                                                                                                        | 1.44 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 850 ms                                                                                                          | 667 ms: 1.27x faster                                                                                                  |
| async_tree_none_tg         | 333 ms                                                                                                          | 291 ms: 1.15x faster                                                                                                  |
| async_tree_io              | 807 ms                                                                                                          | 713 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 421 ms                                                                                                          | 389 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 625 ms                                                                                                          | 580 ms: 1.08x faster                                                                                                  |
| async_tree_none            | 351 ms                                                                                                          | 338 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 623 ms                                                                                                          | 628 ms: 1.01x slower                                                                                                  |
| coroutines                 | 29.9 ms                                                                                                         | 30.4 ms: 1.01x slower                                                                                                 |
| asyncio_websockets         | 649 ms                                                                                                          | 671 ms: 1.03x slower                                                                                                  |
| async_tree_memoization     | 417 ms                                                                                                          | 432 ms: 1.03x slower                                                                                                  |
| async_generators           | 506 ms                                                                                                          | 536 ms: 1.06x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 94.3 ms                                                                                                         | 91.7 ms: 1.03x faster                                                                                                 |
| pidigits       | 223 ms                                                                                                          | 219 ms: 1.02x faster                                                                                                  |
| nbody          | 119 ms                                                                                                          | 159 ms: 1.34x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 29.0 ms                                                                                                         | 27.3 ms: 1.06x faster                                                                                                 |
| regex_effbot   | 3.86 ms                                                                                                         | 3.95 ms: 1.02x slower                                                                                                 |
| regex_dna      | 246 ms                                                                                                          | 253 ms: 1.03x slower                                                                                                  |
| regex_compile  | 154 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 124 ms                                                                                                          | 117 ms: 1.06x faster                                                                                                  |
| xml_etree_parse      | 172 ms                                                                                                          | 173 ms: 1.01x slower                                                                                                  |
| pickle_pure_python   | 387 us                                                                                                          | 425 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 270 us                                                                                                          | 300 us: 1.11x slower                                                                                                  |
| tomli_loads          | 2.49 sec                                                                                                        | 2.78 sec: 1.12x slower                                                                                                |
| json_loads           | 37.2 us                                                                                                         | 41.6 us: 1.12x slower                                                                                                 |
| json_dumps           | 13.7 ms                                                                                                         | 15.4 ms: 1.12x slower                                                                                                 |
| xml_etree_generate   | 109 ms                                                                                                          | 130 ms: 1.19x slower                                                                                                  |
| xml_etree_process    | 74.9 ms                                                                                                         | 92.1 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 17.3 ms                                                                                                         | 22.6 ms: 1.30x slower                                                                                                 |
| python_startup_no_site | 10.2 ms                                                                                                         | 13.8 ms: 1.35x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.33x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 42.8 ms                                                                                                         | 49.4 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 60.9 ms                                                                                                         | 72.2 ms: 1.19x slower                                                                                                 |
| genshi_text     | 25.9 ms                                                                                                         | 33.3 ms: 1.28x slower                                                                                                 |
| mako            | 15.6 ms                                                                                                         | 20.7 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 5.91 ms                                                                                                         | 2.85 ms: 2.07x faster                                                                                                 |
| create_gc_cycles           | 3.12 ms                                                                                                         | 2.20 ms: 1.42x faster                                                                                                 |
| async_tree_io_tg           | 850 ms                                                                                                          | 667 ms: 1.27x faster                                                                                                  |
| async_tree_none_tg         | 333 ms                                                                                                          | 291 ms: 1.15x faster                                                                                                  |
| async_tree_io              | 807 ms                                                                                                          | 713 ms: 1.13x faster                                                                                                  |
| sqlite_synth               | 3.24 us                                                                                                         | 2.95 us: 1.10x faster                                                                                                 |
| bench_mp_pool              | 81.3 ms                                                                                                         | 74.7 ms: 1.09x faster                                                                                                 |
| async_tree_memoization_tg  | 421 ms                                                                                                          | 389 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 625 ms                                                                                                          | 580 ms: 1.08x faster                                                                                                  |
| xml_etree_iterparse        | 124 ms                                                                                                          | 117 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 29.0 ms                                                                                                         | 27.3 ms: 1.06x faster                                                                                                 |
| async_tree_none            | 351 ms                                                                                                          | 338 ms: 1.04x faster                                                                                                  |
| float                      | 94.3 ms                                                                                                         | 91.7 ms: 1.03x faster                                                                                                 |
| pidigits                   | 223 ms                                                                                                          | 219 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 172 ms                                                                                                          | 173 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 623 ms                                                                                                          | 628 ms: 1.01x slower                                                                                                  |
| coroutines                 | 29.9 ms                                                                                                         | 30.4 ms: 1.01x slower                                                                                                 |
| regex_effbot               | 3.86 ms                                                                                                         | 3.95 ms: 1.02x slower                                                                                                 |
| regex_dna                  | 246 ms                                                                                                          | 253 ms: 1.03x slower                                                                                                  |
| asyncio_websockets         | 649 ms                                                                                                          | 671 ms: 1.03x slower                                                                                                  |
| async_tree_memoization     | 417 ms                                                                                                          | 432 ms: 1.03x slower                                                                                                  |
| deltablue                  | 4.30 ms                                                                                                         | 4.48 ms: 1.04x slower                                                                                                 |
| generators                 | 39.3 ms                                                                                                         | 41.1 ms: 1.04x slower                                                                                                 |
| scimark_fft                | 457 ms                                                                                                          | 481 ms: 1.05x slower                                                                                                  |
| dulwich_log                | 73.2 ms                                                                                                         | 77.1 ms: 1.05x slower                                                                                                 |
| json                       | 6.83 ms                                                                                                         | 7.20 ms: 1.06x slower                                                                                                 |
| async_generators           | 506 ms                                                                                                          | 536 ms: 1.06x slower                                                                                                  |
| docutils                   | 3.39 sec                                                                                                        | 3.61 sec: 1.06x slower                                                                                                |
| bench_thread_pool          | 1.77 ms                                                                                                         | 1.89 ms: 1.07x slower                                                                                                 |
| pathlib                    | 23.4 ms                                                                                                         | 25.0 ms: 1.07x slower                                                                                                 |
| scimark_sor                | 146 ms                                                                                                          | 159 ms: 1.09x slower                                                                                                  |
| chaos                      | 73.4 ms                                                                                                         | 80.5 ms: 1.10x slower                                                                                                 |
| spectral_norm              | 129 ms                                                                                                          | 142 ms: 1.10x slower                                                                                                  |
| pickle_pure_python         | 387 us                                                                                                          | 425 us: 1.10x slower                                                                                                  |
| html5lib                   | 75.2 ms                                                                                                         | 82.8 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python       | 270 us                                                                                                          | 300 us: 1.11x slower                                                                                                  |
| 2to3                       | 339 ms                                                                                                          | 378 ms: 1.11x slower                                                                                                  |
| telco                      | 9.44 ms                                                                                                         | 10.5 ms: 1.12x slower                                                                                                 |
| tomli_loads                | 2.49 sec                                                                                                        | 2.78 sec: 1.12x slower                                                                                                |
| json_loads                 | 37.2 us                                                                                                         | 41.6 us: 1.12x slower                                                                                                 |
| pylint                     | 364 ms                                                                                                          | 408 ms: 1.12x slower                                                                                                  |
| sphinx                     | 1.29 sec                                                                                                        | 1.44 sec: 1.12x slower                                                                                                |
| sqlglot_v2_normalize       | 129 ms                                                                                                          | 145 ms: 1.12x slower                                                                                                  |
| json_dumps                 | 13.7 ms                                                                                                         | 15.4 ms: 1.12x slower                                                                                                 |
| bpe_tokeniser              | 5.47 sec                                                                                                        | 6.16 sec: 1.13x slower                                                                                                |
| pyflate                    | 581 ms                                                                                                          | 660 ms: 1.14x slower                                                                                                  |
| nqueens                    | 98.5 ms                                                                                                         | 112 ms: 1.14x slower                                                                                                  |
| pprint_safe_repr           | 890 ms                                                                                                          | 1.01 sec: 1.14x slower                                                                                                |
| many_optionals             | 1.16 ms                                                                                                         | 1.33 ms: 1.14x slower                                                                                                 |
| go                         | 141 ms                                                                                                          | 161 ms: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 3.34 us                                                                                                         | 3.83 us: 1.14x slower                                                                                                 |
| comprehensions             | 21.3 us                                                                                                         | 24.4 us: 1.14x slower                                                                                                 |
| scimark_lu                 | 146 ms                                                                                                          | 166 ms: 1.14x slower                                                                                                  |
| subparsers                 | 30.3 ms                                                                                                         | 34.7 ms: 1.15x slower                                                                                                 |
| k_core                     | 3.27 sec                                                                                                        | 3.75 sec: 1.15x slower                                                                                                |
| logging_silent             | 609 ns                                                                                                          | 699 ns: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.83 sec                                                                                                        | 2.10 sec: 1.15x slower                                                                                                |
| sqlglot_v2_optimize        | 64.2 ms                                                                                                         | 73.8 ms: 1.15x slower                                                                                                 |
| hexiom                     | 7.55 ms                                                                                                         | 8.67 ms: 1.15x slower                                                                                                 |
| raytrace                   | 336 ms                                                                                                          | 386 ms: 1.15x slower                                                                                                  |
| thrift                     | 941 us                                                                                                          | 1.08 ms: 1.15x slower                                                                                                 |
| django_template            | 42.8 ms                                                                                                         | 49.4 ms: 1.15x slower                                                                                                 |
| scimark_sparse_mat_mult    | 6.38 ms                                                                                                         | 7.41 ms: 1.16x slower                                                                                                 |
| regex_compile              | 154 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| deepcopy                   | 322 us                                                                                                          | 375 us: 1.17x slower                                                                                                  |
| sympy_expand               | 552 ms                                                                                                          | 646 ms: 1.17x slower                                                                                                  |
| genshi_xml                 | 60.9 ms                                                                                                         | 72.2 ms: 1.19x slower                                                                                                 |
| xml_etree_generate         | 109 ms                                                                                                          | 130 ms: 1.19x slower                                                                                                  |
| sympy_sum                  | 183 ms                                                                                                          | 219 ms: 1.19x slower                                                                                                  |
| sympy_str                  | 324 ms                                                                                                          | 388 ms: 1.20x slower                                                                                                  |
| logging_format             | 8.80 us                                                                                                         | 10.6 us: 1.20x slower                                                                                                 |
| scimark_monte_carlo        | 83.1 ms                                                                                                         | 100 ms: 1.20x slower                                                                                                  |
| richards                   | 53.6 ms                                                                                                         | 64.6 ms: 1.21x slower                                                                                                 |
| fannkuch                   | 502 ms                                                                                                          | 608 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.54 ms                                                                                                         | 1.87 ms: 1.21x slower                                                                                                 |
| crypto_pyaes               | 91.5 ms                                                                                                         | 111 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.93 ms                                                                                                         | 2.34 ms: 1.22x slower                                                                                                 |
| sympy_integrate            | 23.3 ms                                                                                                         | 28.5 ms: 1.22x slower                                                                                                 |
| richards_super             | 61.6 ms                                                                                                         | 75.1 ms: 1.22x slower                                                                                                 |
| shortest_path              | 707 ms                                                                                                          | 866 ms: 1.22x slower                                                                                                  |
| logging_simple             | 8.18 us                                                                                                         | 10.0 us: 1.23x slower                                                                                                 |
| xml_etree_process          | 74.9 ms                                                                                                         | 92.1 ms: 1.23x slower                                                                                                 |
| meteor_contest             | 128 ms                                                                                                          | 159 ms: 1.24x slower                                                                                                  |
| deepcopy_memo              | 36.8 us                                                                                                         | 45.6 us: 1.24x slower                                                                                                 |
| connected_components       | 629 ms                                                                                                          | 801 ms: 1.27x slower                                                                                                  |
| mdp                        | 1.61 sec                                                                                                        | 2.07 sec: 1.28x slower                                                                                                |
| genshi_text                | 25.9 ms                                                                                                         | 33.3 ms: 1.28x slower                                                                                                 |
| typing_runtime_protocols   | 197 us                                                                                                          | 257 us: 1.30x slower                                                                                                  |
| python_startup             | 17.3 ms                                                                                                         | 22.6 ms: 1.30x slower                                                                                                 |
| mako                       | 15.6 ms                                                                                                         | 20.7 ms: 1.33x slower                                                                                                 |
| nbody                      | 119 ms                                                                                                          | 159 ms: 1.34x slower                                                                                                  |
| coverage                   | 106 ms                                                                                                          | 143 ms: 1.35x slower                                                                                                  |
| python_startup_no_site     | 10.2 ms                                                                                                         | 13.8 ms: 1.35x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmark hidden because not significant (1): pycparser

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.21x