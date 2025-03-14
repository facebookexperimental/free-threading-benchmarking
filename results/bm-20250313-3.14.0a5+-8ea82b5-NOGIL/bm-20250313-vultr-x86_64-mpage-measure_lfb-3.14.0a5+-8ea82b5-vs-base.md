# Results vs. base

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 8ea82b5
- commit date: 2025-03-13
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 290 ms: 1.03x faster                                         |
| docutils       | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                       |
| html5lib       | 72.0 ms                                                                | 70.4 ms: 1.02x faster                                        |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 236 ms                                                                 | 230 ms: 1.03x faster                                         |
| async_tree_memoization     | 339 ms                                                                 | 330 ms: 1.03x faster                                         |
| coroutines                 | 24.1 ms                                                                | 23.5 ms: 1.03x faster                                        |
| async_tree_memoization_tg  | 304 ms                                                                 | 298 ms: 1.02x faster                                         |
| async_tree_none            | 275 ms                                                                 | 269 ms: 1.02x faster                                         |
| async_tree_io              | 583 ms                                                                 | 573 ms: 1.02x faster                                         |
| async_tree_io_tg           | 546 ms                                                                 | 538 ms: 1.01x faster                                         |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 595 ms: 1.06x slower                                         |
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 563 ms: 1.06x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 118 ms: 1.13x faster                                         |
| float          | 77.9 ms                                                                | 71.2 ms: 1.09x faster                                        |
| pidigits       | 202 ms                                                                 | 226 ms: 1.12x slower                                         |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 158 ms                                                                 | 153 ms: 1.04x faster                                         |
| regex_dna      | 184 ms                                                                 | 183 ms: 1.00x faster                                         |
| regex_effbot   | 2.70 ms                                                                | 2.79 ms: 1.03x slower                                        |
| regex_v8       | 23.4 ms                                                                | 24.2 ms: 1.03x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_pure_python | 257 us                                                                 | 238 us: 1.08x faster                                         |
| tomli_loads          | 2.38 sec                                                               | 2.24 sec: 1.06x faster                                       |
| pickle_pure_python   | 360 us                                                                 | 340 us: 1.06x faster                                         |
| xml_etree_process    | 70.4 ms                                                                | 68.7 ms: 1.02x faster                                        |
| json_dumps           | 12.8 ms                                                                | 12.5 ms: 1.02x faster                                        |
| xml_etree_generate   | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                        |
| json_loads           | 29.2 us                                                                | 29.1 us: 1.00x faster                                        |
| xml_etree_iterparse  | 87.7 ms                                                                | 88.2 ms: 1.01x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                        |
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                        |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 28.1 ms                                                                | 26.8 ms: 1.05x faster                                        |
| django_template | 43.1 ms                                                                | 41.8 ms: 1.03x faster                                        |
| mako            | 15.9 ms                                                                | 15.5 ms: 1.03x faster                                        |
| genshi_xml      | 59.6 ms                                                                | 58.6 ms: 1.02x faster                                        |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody                      | 134 ms                                                                 | 118 ms: 1.13x faster                                         |
| go                         | 145 ms                                                                 | 130 ms: 1.12x faster                                         |
| scimark_fft                | 395 ms                                                                 | 357 ms: 1.11x faster                                         |
| scimark_monte_carlo        | 84.1 ms                                                                | 76.0 ms: 1.11x faster                                        |
| float                      | 77.9 ms                                                                | 71.2 ms: 1.09x faster                                        |
| deepcopy_memo              | 38.8 us                                                                | 35.7 us: 1.09x faster                                        |
| fannkuch                   | 499 ms                                                                 | 460 ms: 1.09x faster                                         |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 5.25 ms: 1.08x faster                                        |
| mdp                        | 2.79 sec                                                               | 2.58 sec: 1.08x faster                                       |
| unpickle_pure_python       | 257 us                                                                 | 238 us: 1.08x faster                                         |
| deltablue                  | 3.90 ms                                                                | 3.64 ms: 1.07x faster                                        |
| logging_silent             | 111 ns                                                                 | 104 ns: 1.07x faster                                         |
| raytrace                   | 323 ms                                                                 | 302 ms: 1.07x faster                                         |
| pyflate                    | 509 ms                                                                 | 477 ms: 1.07x faster                                         |
| sqlglot_parse              | 1.61 ms                                                                | 1.51 ms: 1.07x faster                                        |
| deepcopy_reduce            | 3.26 us                                                                | 3.07 us: 1.06x faster                                        |
| scimark_sor                | 136 ms                                                                 | 128 ms: 1.06x faster                                         |
| tomli_loads                | 2.38 sec                                                               | 2.24 sec: 1.06x faster                                       |
| pickle_pure_python         | 360 us                                                                 | 340 us: 1.06x faster                                         |
| chaos                      | 70.1 ms                                                                | 66.3 ms: 1.06x faster                                        |
| sqlglot_transpile          | 1.93 ms                                                                | 1.83 ms: 1.05x faster                                        |
| telco                      | 9.05 ms                                                                | 8.59 ms: 1.05x faster                                        |
| hexiom                     | 7.65 ms                                                                | 7.27 ms: 1.05x faster                                        |
| genshi_text                | 28.1 ms                                                                | 26.8 ms: 1.05x faster                                        |
| pprint_safe_repr           | 848 ms                                                                 | 811 ms: 1.05x faster                                         |
| pprint_pformat             | 1.74 sec                                                               | 1.66 sec: 1.05x faster                                       |
| spectral_norm              | 115 ms                                                                 | 110 ms: 1.05x faster                                         |
| comprehensions             | 21.1 us                                                                | 20.3 us: 1.04x faster                                        |
| deepcopy                   | 312 us                                                                 | 300 us: 1.04x faster                                         |
| richards_super             | 63.7 ms                                                                | 61.4 ms: 1.04x faster                                        |
| subparsers                 | 25.6 ms                                                                | 24.7 ms: 1.04x faster                                        |
| regex_compile              | 158 ms                                                                 | 153 ms: 1.04x faster                                         |
| coverage                   | 99.6 ms                                                                | 96.2 ms: 1.04x faster                                        |
| meteor_contest             | 131 ms                                                                 | 127 ms: 1.03x faster                                         |
| nqueens                    | 97.8 ms                                                                | 94.6 ms: 1.03x faster                                        |
| many_optionals             | 1.18 ms                                                                | 1.14 ms: 1.03x faster                                        |
| richards                   | 55.1 ms                                                                | 53.3 ms: 1.03x faster                                        |
| connected_components       | 504 ms                                                                 | 488 ms: 1.03x faster                                         |
| 2to3                       | 299 ms                                                                 | 290 ms: 1.03x faster                                         |
| django_template            | 43.1 ms                                                                | 41.8 ms: 1.03x faster                                        |
| bpe_tokeniser              | 4.84 sec                                                               | 4.70 sec: 1.03x faster                                       |
| scimark_lu                 | 139 ms                                                                 | 135 ms: 1.03x faster                                         |
| mako                       | 15.9 ms                                                                | 15.5 ms: 1.03x faster                                        |
| crypto_pyaes               | 87.8 ms                                                                | 85.3 ms: 1.03x faster                                        |
| async_tree_none_tg         | 236 ms                                                                 | 230 ms: 1.03x faster                                         |
| sqlglot_normalize          | 121 ms                                                                 | 118 ms: 1.03x faster                                         |
| async_tree_memoization     | 339 ms                                                                 | 330 ms: 1.03x faster                                         |
| coroutines                 | 24.1 ms                                                                | 23.5 ms: 1.03x faster                                        |
| shortest_path              | 548 ms                                                                 | 535 ms: 1.02x faster                                         |
| xml_etree_process          | 70.4 ms                                                                | 68.7 ms: 1.02x faster                                        |
| json_dumps                 | 12.8 ms                                                                | 12.5 ms: 1.02x faster                                        |
| thrift                     | 889 us                                                                 | 869 us: 1.02x faster                                         |
| html5lib                   | 72.0 ms                                                                | 70.4 ms: 1.02x faster                                        |
| sqlglot_optimize           | 61.4 ms                                                                | 60.0 ms: 1.02x faster                                        |
| typing_runtime_protocols   | 197 us                                                                 | 193 us: 1.02x faster                                         |
| async_tree_memoization_tg  | 304 ms                                                                 | 298 ms: 1.02x faster                                         |
| async_tree_none            | 275 ms                                                                 | 269 ms: 1.02x faster                                         |
| async_tree_io              | 583 ms                                                                 | 573 ms: 1.02x faster                                         |
| k_core                     | 2.31 sec                                                               | 2.27 sec: 1.02x faster                                       |
| genshi_xml                 | 59.6 ms                                                                | 58.6 ms: 1.02x faster                                        |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                       |
| async_tree_io_tg           | 546 ms                                                                 | 538 ms: 1.01x faster                                         |
| sympy_integrate            | 24.2 ms                                                                | 23.9 ms: 1.01x faster                                        |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                         |
| sympy_expand               | 551 ms                                                                 | 546 ms: 1.01x faster                                         |
| xml_etree_generate         | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                        |
| json                       | 5.10 ms                                                                | 5.05 ms: 1.01x faster                                        |
| bench_thread_pool          | 3.16 ms                                                                | 3.13 ms: 1.01x faster                                        |
| docutils                   | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                       |
| sympy_str                  | 335 ms                                                                 | 333 ms: 1.00x faster                                         |
| sympy_sum                  | 188 ms                                                                 | 187 ms: 1.00x faster                                         |
| json_loads                 | 29.2 us                                                                | 29.1 us: 1.00x faster                                        |
| regex_dna                  | 184 ms                                                                 | 183 ms: 1.00x faster                                         |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                        |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                        |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.00x slower                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| xml_etree_iterparse        | 87.7 ms                                                                | 88.2 ms: 1.01x slower                                        |
| dulwich_log                | 73.0 ms                                                                | 73.6 ms: 1.01x slower                                        |
| generators                 | 31.6 ms                                                                | 32.1 ms: 1.02x slower                                        |
| sqlite_synth               | 2.02 us                                                                | 2.06 us: 1.02x slower                                        |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.02x slower                                        |
| regex_effbot               | 2.70 ms                                                                | 2.79 ms: 1.03x slower                                        |
| regex_v8                   | 23.4 ms                                                                | 24.2 ms: 1.03x slower                                        |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 595 ms: 1.06x slower                                         |
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 563 ms: 1.06x slower                                         |
| pidigits                   | 202 ms                                                                 | 226 ms: 1.12x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (9): sphinx, pylint, create_gc_cycles, gc_traversal, logging_format, xml_etree_parse, logging_simple, bench_mp_pool, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x