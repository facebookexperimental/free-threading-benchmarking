# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 8ea82b5
- commit date: 2025-03-13
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 290 ms: 1.12x slower                                         |
| docutils       | 2.61 sec                                                               | 2.78 sec: 1.07x slower                                       |
| sphinx         | 995 ms                                                                 | 1.09 sec: 1.09x slower                                       |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 538 ms: 1.17x faster                                         |
| async_tree_none_tg         | 267 ms                                                                 | 230 ms: 1.16x faster                                         |
| async_tree_io              | 630 ms                                                                 | 573 ms: 1.10x faster                                         |
| async_tree_memoization_tg  | 318 ms                                                                 | 298 ms: 1.07x faster                                         |
| async_tree_none            | 277 ms                                                                 | 269 ms: 1.03x faster                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                        |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                         |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 563 ms: 1.12x slower                                         |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 595 ms: 1.15x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                 |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 75.8 ms                                                                | 71.2 ms: 1.06x faster                                        |
| nbody          | 102 ms                                                                 | 118 ms: 1.16x slower                                         |
| pidigits       | 187 ms                                                                 | 226 ms: 1.21x slower                                         |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 24.2 ms: 1.01x faster                                        |
| regex_effbot   | 2.77 ms                                                                | 2.79 ms: 1.00x slower                                        |
| regex_dna      | 179 ms                                                                 | 183 ms: 1.02x slower                                         |
| regex_compile  | 130 ms                                                                 | 153 ms: 1.18x slower                                         |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 93.4 ms                                                                | 88.2 ms: 1.06x faster                                        |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                         |
| pickle_pure_python   | 324 us                                                                 | 340 us: 1.05x slower                                         |
| unpickle_pure_python | 224 us                                                                 | 238 us: 1.06x slower                                         |
| json_loads           | 27.0 us                                                                | 29.1 us: 1.08x slower                                        |
| xml_etree_generate   | 86.5 ms                                                                | 95.7 ms: 1.11x slower                                        |
| json_dumps           | 11.2 ms                                                                | 12.5 ms: 1.12x slower                                        |
| tomli_loads          | 2.00 sec                                                               | 2.24 sec: 1.12x slower                                       |
| xml_etree_process    | 60.1 ms                                                                | 68.7 ms: 1.14x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                        |
| python_startup_no_site | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                        |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 37.2 ms                                                                | 41.8 ms: 1.12x slower                                        |
| genshi_xml      | 51.0 ms                                                                | 58.6 ms: 1.15x slower                                        |
| genshi_text     | 21.9 ms                                                                | 26.8 ms: 1.23x slower                                        |
| mako            | 12.1 ms                                                                | 15.5 ms: 1.28x slower                                        |
| Geometric mean  | (ref)                                                                  | 1.19x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| gc_traversal               | 4.76 ms                                                                | 1.74 ms: 2.74x faster                                        |
| create_gc_cycles           | 1.83 ms                                                                | 1.33 ms: 1.37x faster                                        |
| async_tree_io_tg           | 628 ms                                                                 | 538 ms: 1.17x faster                                         |
| async_tree_none_tg         | 267 ms                                                                 | 230 ms: 1.16x faster                                         |
| async_tree_io              | 630 ms                                                                 | 573 ms: 1.10x faster                                         |
| sqlite_synth               | 2.21 us                                                                | 2.06 us: 1.07x faster                                        |
| async_tree_memoization_tg  | 318 ms                                                                 | 298 ms: 1.07x faster                                         |
| float                      | 75.8 ms                                                                | 71.2 ms: 1.06x faster                                        |
| xml_etree_iterparse        | 93.4 ms                                                                | 88.2 ms: 1.06x faster                                        |
| async_tree_none            | 277 ms                                                                 | 269 ms: 1.03x faster                                         |
| regex_v8                   | 24.5 ms                                                                | 24.2 ms: 1.01x faster                                        |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| regex_effbot               | 2.77 ms                                                                | 2.79 ms: 1.00x slower                                        |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                        |
| pycparser                  | 1.16 sec                                                               | 1.17 sec: 1.01x slower                                       |
| pathlib                    | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                        |
| regex_dna                  | 179 ms                                                                 | 183 ms: 1.02x slower                                         |
| mdp                        | 2.50 sec                                                               | 2.58 sec: 1.03x slower                                       |
| json                       | 4.89 ms                                                                | 5.05 ms: 1.03x slower                                        |
| logging_silent             | 99.6 ns                                                                | 104 ns: 1.05x slower                                         |
| pickle_pure_python         | 324 us                                                                 | 340 us: 1.05x slower                                         |
| python_startup             | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                        |
| bpe_tokeniser              | 4.43 sec                                                               | 4.70 sec: 1.06x slower                                       |
| unpickle_pure_python       | 224 us                                                                 | 238 us: 1.06x slower                                         |
| scimark_fft                | 334 ms                                                                 | 357 ms: 1.07x slower                                         |
| docutils                   | 2.61 sec                                                               | 2.78 sec: 1.07x slower                                       |
| json_loads                 | 27.0 us                                                                | 29.1 us: 1.08x slower                                        |
| generators                 | 29.7 ms                                                                | 32.1 ms: 1.08x slower                                        |
| subparsers                 | 22.7 ms                                                                | 24.7 ms: 1.09x slower                                        |
| dulwich_log                | 67.5 ms                                                                | 73.6 ms: 1.09x slower                                        |
| bench_mp_pool              | 88.2 ms                                                                | 96.2 ms: 1.09x slower                                        |
| sphinx                     | 995 ms                                                                 | 1.09 sec: 1.09x slower                                       |
| many_optionals             | 1.04 ms                                                                | 1.14 ms: 1.10x slower                                        |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                         |
| pprint_safe_repr           | 737 ms                                                                 | 811 ms: 1.10x slower                                         |
| scimark_sor                | 116 ms                                                                 | 128 ms: 1.10x slower                                         |
| k_core                     | 2.06 sec                                                               | 2.27 sec: 1.10x slower                                       |
| pylint                     | 285 ms                                                                 | 315 ms: 1.10x slower                                         |
| xml_etree_generate         | 86.5 ms                                                                | 95.7 ms: 1.11x slower                                        |
| pprint_pformat             | 1.50 sec                                                               | 1.66 sec: 1.11x slower                                       |
| json_dumps                 | 11.2 ms                                                                | 12.5 ms: 1.12x slower                                        |
| scimark_sparse_mat_mult    | 4.70 ms                                                                | 5.25 ms: 1.12x slower                                        |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 563 ms: 1.12x slower                                         |
| tomli_loads                | 2.00 sec                                                               | 2.24 sec: 1.12x slower                                       |
| pyflate                    | 425 ms                                                                 | 477 ms: 1.12x slower                                         |
| django_template            | 37.2 ms                                                                | 41.8 ms: 1.12x slower                                        |
| 2to3                       | 258 ms                                                                 | 290 ms: 1.12x slower                                         |
| telco                      | 7.64 ms                                                                | 8.59 ms: 1.12x slower                                        |
| deepcopy_reduce            | 2.73 us                                                                | 3.07 us: 1.12x slower                                        |
| sqlglot_normalize          | 104 ms                                                                 | 118 ms: 1.13x slower                                         |
| raytrace                   | 267 ms                                                                 | 302 ms: 1.13x slower                                         |
| sqlglot_transpile          | 1.62 ms                                                                | 1.83 ms: 1.13x slower                                        |
| chaos                      | 58.5 ms                                                                | 66.3 ms: 1.13x slower                                        |
| sqlglot_optimize           | 52.7 ms                                                                | 60.0 ms: 1.14x slower                                        |
| scimark_monte_carlo        | 66.6 ms                                                                | 76.0 ms: 1.14x slower                                        |
| spectral_norm              | 95.9 ms                                                                | 110 ms: 1.14x slower                                         |
| xml_etree_process          | 60.1 ms                                                                | 68.7 ms: 1.14x slower                                        |
| go                         | 113 ms                                                                 | 130 ms: 1.14x slower                                         |
| sqlglot_parse              | 1.32 ms                                                                | 1.51 ms: 1.15x slower                                        |
| fannkuch                   | 401 ms                                                                 | 460 ms: 1.15x slower                                         |
| deepcopy                   | 261 us                                                                 | 300 us: 1.15x slower                                         |
| genshi_xml                 | 51.0 ms                                                                | 58.6 ms: 1.15x slower                                        |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 595 ms: 1.15x slower                                         |
| thrift                     | 754 us                                                                 | 869 us: 1.15x slower                                         |
| nbody                      | 102 ms                                                                 | 118 ms: 1.16x slower                                         |
| deepcopy_memo              | 30.8 us                                                                | 35.7 us: 1.16x slower                                        |
| nqueens                    | 81.4 ms                                                                | 94.6 ms: 1.16x slower                                        |
| deltablue                  | 3.12 ms                                                                | 3.64 ms: 1.17x slower                                        |
| sympy_expand               | 465 ms                                                                 | 546 ms: 1.17x slower                                         |
| comprehensions             | 17.2 us                                                                | 20.3 us: 1.18x slower                                        |
| regex_compile              | 130 ms                                                                 | 153 ms: 1.18x slower                                         |
| scimark_lu                 | 114 ms                                                                 | 135 ms: 1.18x slower                                         |
| coverage                   | 81.1 ms                                                                | 96.2 ms: 1.19x slower                                        |
| sympy_integrate            | 20.1 ms                                                                | 23.9 ms: 1.19x slower                                        |
| hexiom                     | 6.10 ms                                                                | 7.27 ms: 1.19x slower                                        |
| crypto_pyaes               | 71.5 ms                                                                | 85.3 ms: 1.19x slower                                        |
| logging_simple             | 6.05 us                                                                | 7.23 us: 1.19x slower                                        |
| sympy_str                  | 278 ms                                                                 | 333 ms: 1.20x slower                                         |
| sympy_sum                  | 156 ms                                                                 | 187 ms: 1.20x slower                                         |
| shortest_path              | 445 ms                                                                 | 535 ms: 1.20x slower                                         |
| sqlalchemy_declarative     | 131 ms                                                                 | 158 ms: 1.20x slower                                         |
| pidigits                   | 187 ms                                                                 | 226 ms: 1.21x slower                                         |
| sqlalchemy_imperative      | 19.8 ms                                                                | 24.0 ms: 1.21x slower                                        |
| connected_components       | 402 ms                                                                 | 488 ms: 1.21x slower                                         |
| typing_runtime_protocols   | 158 us                                                                 | 193 us: 1.22x slower                                         |
| genshi_text                | 21.9 ms                                                                | 26.8 ms: 1.23x slower                                        |
| logging_format             | 6.73 us                                                                | 8.26 us: 1.23x slower                                        |
| richards_super             | 49.8 ms                                                                | 61.4 ms: 1.23x slower                                        |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                         |
| richards                   | 42.7 ms                                                                | 53.3 ms: 1.25x slower                                        |
| mako                       | 12.1 ms                                                                | 15.5 ms: 1.28x slower                                        |
| python_startup_no_site     | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                        |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 2.97x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                 |

Benchmark hidden because not significant (1): async_tree_memoization
Ignored benchmarks (1) of results/bm-20250313-3.14.0a5+-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5.json: html5lib

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x