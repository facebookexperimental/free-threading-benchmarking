# Results vs. base

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 76fc3d1
- commit date: 2025-03-14
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 249 ms: 1.04x faster                                         |
| docutils       | 2.61 sec                                                               | 2.59 sec: 1.01x faster                                       |
| sphinx         | 995 ms                                                                 | 985 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 267 ms                                                                 | 258 ms: 1.04x faster                                         |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 488 ms: 1.03x faster                                         |
| async_generators           | 339 ms                                                                 | 329 ms: 1.03x faster                                         |
| async_tree_none            | 277 ms                                                                 | 268 ms: 1.03x faster                                         |
| async_tree_memoization     | 329 ms                                                                 | 321 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 503 ms: 1.03x faster                                         |
| async_tree_io_tg           | 628 ms                                                                 | 614 ms: 1.02x faster                                         |
| coroutines                 | 23.4 ms                                                                | 22.9 ms: 1.02x faster                                        |
| async_tree_io              | 630 ms                                                                 | 618 ms: 1.02x faster                                         |
| async_tree_memoization_tg  | 318 ms                                                                 | 313 ms: 1.02x faster                                         |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 102 ms                                                                 | 86.0 ms: 1.19x faster                                        |
| float          | 75.8 ms                                                                | 69.4 ms: 1.09x faster                                        |
| pidigits       | 187 ms                                                                 | 208 ms: 1.11x slower                                         |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 130 ms                                                                 | 125 ms: 1.03x faster                                         |
| regex_dna      | 179 ms                                                                 | 177 ms: 1.01x faster                                         |
| regex_effbot   | 2.77 ms                                                                | 2.84 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.00 sec                                                               | 1.89 sec: 1.06x faster                                       |
| pickle_pure_python   | 324 us                                                                 | 309 us: 1.05x faster                                         |
| unpickle_pure_python | 224 us                                                                 | 214 us: 1.05x faster                                         |
| xml_etree_generate   | 86.5 ms                                                                | 83.1 ms: 1.04x faster                                        |
| xml_etree_iterparse  | 93.4 ms                                                                | 91.6 ms: 1.02x faster                                        |
| xml_etree_process    | 60.1 ms                                                                | 59.0 ms: 1.02x faster                                        |
| json_dumps           | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                        |
| json_loads           | 27.0 us                                                                | 27.7 us: 1.03x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 8.63 ms                                                                | 8.60 ms: 1.00x faster                                        |
| python_startup         | 14.9 ms                                                                | 15.0 ms: 1.00x slower                                        |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 21.9 ms                                                                | 20.6 ms: 1.06x faster                                        |
| django_template | 37.2 ms                                                                | 35.5 ms: 1.05x faster                                        |
| genshi_xml      | 51.0 ms                                                                | 48.8 ms: 1.05x faster                                        |
| mako            | 12.1 ms                                                                | 11.6 ms: 1.05x faster                                        |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody                      | 102 ms                                                                 | 86.0 ms: 1.19x faster                                        |
| gc_traversal               | 4.76 ms                                                                | 4.32 ms: 1.10x faster                                        |
| float                      | 75.8 ms                                                                | 69.4 ms: 1.09x faster                                        |
| scimark_monte_carlo        | 66.6 ms                                                                | 61.3 ms: 1.09x faster                                        |
| scimark_fft                | 334 ms                                                                 | 309 ms: 1.08x faster                                         |
| sqlglot_parse              | 1.32 ms                                                                | 1.23 ms: 1.07x faster                                        |
| generators                 | 29.7 ms                                                                | 27.7 ms: 1.07x faster                                        |
| deepcopy_memo              | 30.8 us                                                                | 28.9 us: 1.07x faster                                        |
| raytrace                   | 267 ms                                                                 | 251 ms: 1.07x faster                                         |
| genshi_text                | 21.9 ms                                                                | 20.6 ms: 1.06x faster                                        |
| tomli_loads                | 2.00 sec                                                               | 1.89 sec: 1.06x faster                                       |
| chaos                      | 58.5 ms                                                                | 55.2 ms: 1.06x faster                                        |
| sqlglot_transpile          | 1.62 ms                                                                | 1.53 ms: 1.06x faster                                        |
| scimark_sor                | 116 ms                                                                 | 110 ms: 1.06x faster                                         |
| spectral_norm              | 95.9 ms                                                                | 91.1 ms: 1.05x faster                                        |
| django_template            | 37.2 ms                                                                | 35.5 ms: 1.05x faster                                        |
| go                         | 113 ms                                                                 | 108 ms: 1.05x faster                                         |
| pickle_pure_python         | 324 us                                                                 | 309 us: 1.05x faster                                         |
| pyflate                    | 425 ms                                                                 | 406 ms: 1.05x faster                                         |
| unpickle_pure_python       | 224 us                                                                 | 214 us: 1.05x faster                                         |
| genshi_xml                 | 51.0 ms                                                                | 48.8 ms: 1.05x faster                                        |
| crypto_pyaes               | 71.5 ms                                                                | 68.4 ms: 1.05x faster                                        |
| richards_super             | 49.8 ms                                                                | 47.6 ms: 1.05x faster                                        |
| mako                       | 12.1 ms                                                                | 11.6 ms: 1.05x faster                                        |
| pycparser                  | 1.16 sec                                                               | 1.11 sec: 1.05x faster                                       |
| fannkuch                   | 401 ms                                                                 | 384 ms: 1.04x faster                                         |
| comprehensions             | 17.2 us                                                                | 16.5 us: 1.04x faster                                        |
| xml_etree_generate         | 86.5 ms                                                                | 83.1 ms: 1.04x faster                                        |
| hexiom                     | 6.10 ms                                                                | 5.88 ms: 1.04x faster                                        |
| scimark_sparse_mat_mult    | 4.70 ms                                                                | 4.54 ms: 1.04x faster                                        |
| 2to3                       | 258 ms                                                                 | 249 ms: 1.04x faster                                         |
| async_tree_none_tg         | 267 ms                                                                 | 258 ms: 1.04x faster                                         |
| deepcopy                   | 261 us                                                                 | 252 us: 1.04x faster                                         |
| regex_compile              | 130 ms                                                                 | 125 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 488 ms: 1.03x faster                                         |
| sqlglot_optimize           | 52.7 ms                                                                | 51.0 ms: 1.03x faster                                        |
| async_generators           | 339 ms                                                                 | 329 ms: 1.03x faster                                         |
| async_tree_none            | 277 ms                                                                 | 268 ms: 1.03x faster                                         |
| mdp                        | 2.50 sec                                                               | 2.42 sec: 1.03x faster                                       |
| deepcopy_reduce            | 2.73 us                                                                | 2.65 us: 1.03x faster                                        |
| pprint_pformat             | 1.50 sec                                                               | 1.46 sec: 1.03x faster                                       |
| pprint_safe_repr           | 737 ms                                                                 | 716 ms: 1.03x faster                                         |
| bpe_tokeniser              | 4.43 sec                                                               | 4.30 sec: 1.03x faster                                       |
| richards                   | 42.7 ms                                                                | 41.5 ms: 1.03x faster                                        |
| async_tree_memoization     | 329 ms                                                                 | 321 ms: 1.03x faster                                         |
| meteor_contest             | 101 ms                                                                 | 98.8 ms: 1.03x faster                                        |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 503 ms: 1.03x faster                                         |
| nqueens                    | 81.4 ms                                                                | 79.5 ms: 1.02x faster                                        |
| sqlglot_normalize          | 104 ms                                                                 | 102 ms: 1.02x faster                                         |
| async_tree_io_tg           | 628 ms                                                                 | 614 ms: 1.02x faster                                         |
| connected_components       | 402 ms                                                                 | 393 ms: 1.02x faster                                         |
| many_optionals             | 1.04 ms                                                                | 1.02 ms: 1.02x faster                                        |
| telco                      | 7.64 ms                                                                | 7.49 ms: 1.02x faster                                        |
| coroutines                 | 23.4 ms                                                                | 22.9 ms: 1.02x faster                                        |
| logging_silent             | 99.6 ns                                                                | 97.5 ns: 1.02x faster                                        |
| async_tree_io              | 630 ms                                                                 | 618 ms: 1.02x faster                                         |
| thrift                     | 754 us                                                                 | 739 us: 1.02x faster                                         |
| xml_etree_iterparse        | 93.4 ms                                                                | 91.6 ms: 1.02x faster                                        |
| typing_runtime_protocols   | 158 us                                                                 | 155 us: 1.02x faster                                         |
| shortest_path              | 445 ms                                                                 | 437 ms: 1.02x faster                                         |
| xml_etree_process          | 60.1 ms                                                                | 59.0 ms: 1.02x faster                                        |
| sympy_str                  | 278 ms                                                                 | 274 ms: 1.02x faster                                         |
| scimark_lu                 | 114 ms                                                                 | 112 ms: 1.02x faster                                         |
| sympy_integrate            | 20.1 ms                                                                | 19.8 ms: 1.02x faster                                        |
| async_tree_memoization_tg  | 318 ms                                                                 | 313 ms: 1.02x faster                                         |
| k_core                     | 2.06 sec                                                               | 2.03 sec: 1.01x faster                                       |
| regex_dna                  | 179 ms                                                                 | 177 ms: 1.01x faster                                         |
| pathlib                    | 19.6 ms                                                                | 19.3 ms: 1.01x faster                                        |
| sphinx                     | 995 ms                                                                 | 985 ms: 1.01x faster                                         |
| bench_thread_pool          | 1.05 ms                                                                | 1.04 ms: 1.01x faster                                        |
| sympy_expand               | 465 ms                                                                 | 461 ms: 1.01x faster                                         |
| docutils                   | 2.61 sec                                                               | 2.59 sec: 1.01x faster                                       |
| sqlalchemy_declarative     | 131 ms                                                                 | 130 ms: 1.01x faster                                         |
| python_startup_no_site     | 8.63 ms                                                                | 8.60 ms: 1.00x faster                                        |
| python_startup             | 14.9 ms                                                                | 15.0 ms: 1.00x slower                                        |
| json_dumps                 | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                        |
| logging_simple             | 6.05 us                                                                | 6.12 us: 1.01x slower                                        |
| logging_format             | 6.73 us                                                                | 6.82 us: 1.01x slower                                        |
| json                       | 4.89 ms                                                                | 4.97 ms: 1.02x slower                                        |
| sqlalchemy_imperative      | 19.8 ms                                                                | 20.1 ms: 1.02x slower                                        |
| regex_effbot               | 2.77 ms                                                                | 2.84 ms: 1.02x slower                                        |
| json_loads                 | 27.0 us                                                                | 27.7 us: 1.03x slower                                        |
| deltablue                  | 3.12 ms                                                                | 3.25 ms: 1.04x slower                                        |
| pidigits                   | 187 ms                                                                 | 208 ms: 1.11x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (11): pylint, subparsers, xml_etree_parse, coverage, bench_mp_pool, dulwich_log, sympy_sum, asyncio_websockets, regex_v8, sqlite_synth, create_gc_cycles

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x