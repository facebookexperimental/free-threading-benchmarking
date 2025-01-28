# Results vs. base

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.152x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 489 ms                                                                                                            | 550 ms: 1.13x slower                                                                                                    |
| html5lib       | 89.1 ms                                                                                                           | 114 ms: 1.27x slower                                                                                                    |
| sphinx         | 1.44 sec                                                                                                          | 1.70 sec: 1.18x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg        | 407 ms                                                                                                            | 351 ms: 1.16x faster                                                                                                    |
| async_tree_io_tg          | 969 ms                                                                                                            | 859 ms: 1.13x faster                                                                                                    |
| async_tree_io             | 954 ms                                                                                                            | 897 ms: 1.06x faster                                                                                                    |
| asyncio_websockets        | 722 ms                                                                                                            | 776 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 738 ms                                                                                                            | 794 ms: 1.08x slower                                                                                                    |
| async_tree_memoization_tg | 494 ms                                                                                                            | 542 ms: 1.10x slower                                                                                                    |
| async_tree_memoization    | 509 ms                                                                                                            | 563 ms: 1.11x slower                                                                                                    |
| async_tree_none           | 392 ms                                                                                                            | 448 ms: 1.14x slower                                                                                                    |
| async_generators          | 537 ms                                                                                                            | 618 ms: 1.15x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 117 ms                                                                                                            | 183 ms: 1.57x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.11 ms                                                                                                           | 4.75 ms: 1.16x slower                                                                                                   |
| regex_compile  | 173 ms                                                                                                            | 225 ms: 1.30x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_pure_python   | 467 us                                                                                                            | 505 us: 1.08x slower                                                                                                    |
| xml_etree_parse      | 213 ms                                                                                                            | 236 ms: 1.11x slower                                                                                                    |
| tomli_loads          | 2.73 sec                                                                                                          | 3.15 sec: 1.15x slower                                                                                                  |
| xml_etree_generate   | 119 ms                                                                                                            | 140 ms: 1.17x slower                                                                                                    |
| json_loads           | 36.8 us                                                                                                           | 43.1 us: 1.17x slower                                                                                                   |
| xml_etree_process    | 84.2 ms                                                                                                           | 107 ms: 1.27x slower                                                                                                    |
| unpickle_pure_python | 288 us                                                                                                            | 376 us: 1.31x slower                                                                                                    |
| json_dumps           | 14.7 ms                                                                                                           | 19.7 ms: 1.34x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 27.4 ms                                                                                                           | 31.9 ms: 1.16x slower                                                                                                   |
| python_startup_no_site | 16.3 ms                                                                                                           | 21.7 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 46.8 ms                                                                                                           | 62.4 ms: 1.33x slower                                                                                                   |
| genshi_text     | 27.4 ms                                                                                                           | 37.8 ms: 1.38x slower                                                                                                   |
| genshi_xml      | 66.2 ms                                                                                                           | 92.3 ms: 1.39x slower                                                                                                   |
| mako            | 17.9 ms                                                                                                           | 25.0 ms: 1.40x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.38x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles          | 4.45 ms                                                                                                           | 3.19 ms: 1.40x faster                                                                                                   |
| sqlite_synth              | 4.28 us                                                                                                           | 3.65 us: 1.17x faster                                                                                                   |
| async_tree_none_tg        | 407 ms                                                                                                            | 351 ms: 1.16x faster                                                                                                    |
| async_tree_io_tg          | 969 ms                                                                                                            | 859 ms: 1.13x faster                                                                                                    |
| async_tree_io             | 954 ms                                                                                                            | 897 ms: 1.06x faster                                                                                                    |
| scimark_lu                | 172 ms                                                                                                            | 181 ms: 1.05x slower                                                                                                    |
| sympy_integrate           | 30.1 ms                                                                                                           | 31.9 ms: 1.06x slower                                                                                                   |
| shortest_path             | 972 ms                                                                                                            | 1.04 sec: 1.07x slower                                                                                                  |
| asyncio_websockets        | 722 ms                                                                                                            | 776 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 738 ms                                                                                                            | 794 ms: 1.08x slower                                                                                                    |
| pickle_pure_python        | 467 us                                                                                                            | 505 us: 1.08x slower                                                                                                    |
| coverage                  | 128 ms                                                                                                            | 139 ms: 1.08x slower                                                                                                    |
| sqlglot_optimize          | 79.3 ms                                                                                                           | 86.8 ms: 1.09x slower                                                                                                   |
| pycparser                 | 1.54 sec                                                                                                          | 1.69 sec: 1.10x slower                                                                                                  |
| async_tree_memoization_tg | 494 ms                                                                                                            | 542 ms: 1.10x slower                                                                                                    |
| k_core                    | 4.21 sec                                                                                                          | 4.65 sec: 1.11x slower                                                                                                  |
| async_tree_memoization    | 509 ms                                                                                                            | 563 ms: 1.11x slower                                                                                                    |
| xml_etree_parse           | 213 ms                                                                                                            | 236 ms: 1.11x slower                                                                                                    |
| logging_silent            | 148 ns                                                                                                            | 165 ns: 1.11x slower                                                                                                    |
| pathlib                   | 28.6 ms                                                                                                           | 31.9 ms: 1.12x slower                                                                                                   |
| 2to3                      | 489 ms                                                                                                            | 550 ms: 1.13x slower                                                                                                    |
| mdp                       | 3.74 sec                                                                                                          | 4.26 sec: 1.14x slower                                                                                                  |
| async_tree_none           | 392 ms                                                                                                            | 448 ms: 1.14x slower                                                                                                    |
| nqueens                   | 108 ms                                                                                                            | 124 ms: 1.15x slower                                                                                                    |
| async_generators          | 537 ms                                                                                                            | 618 ms: 1.15x slower                                                                                                    |
| tomli_loads               | 2.73 sec                                                                                                          | 3.15 sec: 1.15x slower                                                                                                  |
| sympy_str                 | 419 ms                                                                                                            | 483 ms: 1.15x slower                                                                                                    |
| scimark_fft               | 503 ms                                                                                                            | 580 ms: 1.15x slower                                                                                                    |
| regex_effbot              | 4.11 ms                                                                                                           | 4.75 ms: 1.16x slower                                                                                                   |
| connected_components      | 823 ms                                                                                                            | 953 ms: 1.16x slower                                                                                                    |
| sqlglot_transpile         | 2.44 ms                                                                                                           | 2.83 ms: 1.16x slower                                                                                                   |
| python_startup            | 27.4 ms                                                                                                           | 31.9 ms: 1.16x slower                                                                                                   |
| many_optionals            | 1.24 ms                                                                                                           | 1.45 ms: 1.17x slower                                                                                                   |
| xml_etree_generate        | 119 ms                                                                                                            | 140 ms: 1.17x slower                                                                                                    |
| json_loads                | 36.8 us                                                                                                           | 43.1 us: 1.17x slower                                                                                                   |
| sympy_expand              | 678 ms                                                                                                            | 798 ms: 1.18x slower                                                                                                    |
| sphinx                    | 1.44 sec                                                                                                          | 1.70 sec: 1.18x slower                                                                                                  |
| json                      | 7.35 ms                                                                                                           | 8.76 ms: 1.19x slower                                                                                                   |
| scimark_monte_carlo       | 99.0 ms                                                                                                           | 119 ms: 1.21x slower                                                                                                    |
| sqlalchemy_imperative     | 25.3 ms                                                                                                           | 30.5 ms: 1.21x slower                                                                                                   |
| sqlglot_normalize         | 152 ms                                                                                                            | 186 ms: 1.23x slower                                                                                                    |
| pprint_pformat            | 1.90 sec                                                                                                          | 2.35 sec: 1.24x slower                                                                                                  |
| pylint                    | 393 ms                                                                                                            | 488 ms: 1.24x slower                                                                                                    |
| crypto_pyaes              | 98.8 ms                                                                                                           | 123 ms: 1.24x slower                                                                                                    |
| raytrace                  | 394 ms                                                                                                            | 493 ms: 1.25x slower                                                                                                    |
| spectral_norm             | 135 ms                                                                                                            | 170 ms: 1.26x slower                                                                                                    |
| richards_super            | 72.1 ms                                                                                                           | 91.4 ms: 1.27x slower                                                                                                   |
| xml_etree_process         | 84.2 ms                                                                                                           | 107 ms: 1.27x slower                                                                                                    |
| dulwich_log               | 93.1 ms                                                                                                           | 118 ms: 1.27x slower                                                                                                    |
| html5lib                  | 89.1 ms                                                                                                           | 114 ms: 1.27x slower                                                                                                    |
| richards                  | 63.1 ms                                                                                                           | 80.5 ms: 1.28x slower                                                                                                   |
| logging_format            | 9.16 us                                                                                                           | 11.8 us: 1.29x slower                                                                                                   |
| scimark_sor               | 153 ms                                                                                                            | 197 ms: 1.29x slower                                                                                                    |
| pyflate                   | 649 ms                                                                                                            | 840 ms: 1.29x slower                                                                                                    |
| comprehensions            | 24.1 us                                                                                                           | 31.2 us: 1.30x slower                                                                                                   |
| regex_compile             | 173 ms                                                                                                            | 225 ms: 1.30x slower                                                                                                    |
| pprint_safe_repr          | 927 ms                                                                                                            | 1.21 sec: 1.30x slower                                                                                                  |
| unpickle_pure_python      | 288 us                                                                                                            | 376 us: 1.31x slower                                                                                                    |
| bpe_tokeniser             | 6.02 sec                                                                                                          | 7.96 sec: 1.32x slower                                                                                                  |
| fannkuch                  | 509 ms                                                                                                            | 673 ms: 1.32x slower                                                                                                    |
| python_startup_no_site    | 16.3 ms                                                                                                           | 21.7 ms: 1.33x slower                                                                                                   |
| django_template           | 46.8 ms                                                                                                           | 62.4 ms: 1.33x slower                                                                                                   |
| sqlalchemy_declarative    | 194 ms                                                                                                            | 258 ms: 1.33x slower                                                                                                    |
| meteor_contest            | 154 ms                                                                                                            | 206 ms: 1.34x slower                                                                                                    |
| json_dumps                | 14.7 ms                                                                                                           | 19.7 ms: 1.34x slower                                                                                                   |
| deepcopy_memo             | 43.0 us                                                                                                           | 57.6 us: 1.34x slower                                                                                                   |
| telco                     | 9.90 ms                                                                                                           | 13.3 ms: 1.34x slower                                                                                                   |
| genshi_text               | 27.4 ms                                                                                                           | 37.8 ms: 1.38x slower                                                                                                   |
| deepcopy_reduce           | 3.67 us                                                                                                           | 5.06 us: 1.38x slower                                                                                                   |
| chaos                     | 76.8 ms                                                                                                           | 106 ms: 1.38x slower                                                                                                    |
| genshi_xml                | 66.2 ms                                                                                                           | 92.3 ms: 1.39x slower                                                                                                   |
| mako                      | 17.9 ms                                                                                                           | 25.0 ms: 1.40x slower                                                                                                   |
| thrift                    | 975 us                                                                                                            | 1.37 ms: 1.41x slower                                                                                                   |
| sqlglot_parse             | 1.71 ms                                                                                                           | 2.44 ms: 1.43x slower                                                                                                   |
| go                        | 162 ms                                                                                                            | 232 ms: 1.44x slower                                                                                                    |
| hexiom                    | 8.59 ms                                                                                                           | 12.4 ms: 1.44x slower                                                                                                   |
| logging_simple            | 8.14 us                                                                                                           | 11.8 us: 1.45x slower                                                                                                   |
| scimark_sparse_mat_mult   | 6.06 ms                                                                                                           | 8.94 ms: 1.48x slower                                                                                                   |
| deltablue                 | 4.54 ms                                                                                                           | 6.71 ms: 1.48x slower                                                                                                   |
| typing_runtime_protocols  | 205 us                                                                                                            | 310 us: 1.52x slower                                                                                                    |
| nbody                     | 117 ms                                                                                                            | 183 ms: 1.57x slower                                                                                                    |
| sympy_sum                 | 191 ms                                                                                                            | 299 ms: 1.57x slower                                                                                                    |
| deepcopy                  | 327 us                                                                                                            | 520 us: 1.59x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (13): regex_v8, pidigits, async_tree_cpu_io_mixed_tg, bench_mp_pool, docutils, float, coroutines, generators, regex_dna, xml_etree_iterparse, gc_traversal, subparsers, bench_thread_pool

- Geometric mean (including insignificant results): 1.152x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.19x