# Results vs. base

- fork: kumaraditya303
- ref: asyncio_tsafe
- machine: linux-x86_64
- commit hash: 41a86a6
- commit date: 2025-01-01
- overall geometric mean: 1.008x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 350 ms                                                                 | 352 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 24.6 ms                                                                | 24.4 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 567 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 590 ms                                                                 | 599 ms: 1.02x slower                                                    |
| async_tree_none            | 345 ms                                                                 | 351 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 309 ms                                                                 | 314 ms: 1.02x slower                                                    |
| async_tree_io              | 748 ms                                                                 | 764 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 391 ms                                                                 | 400 ms: 1.02x slower                                                    |
| async_tree_memoization     | 419 ms                                                                 | 429 ms: 1.02x slower                                                    |
| async_tree_io_tg           | 721 ms                                                                 | 740 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 182 ms: 1.05x faster                                                    |
| float          | 108 ms                                                                 | 108 ms: 1.00x slower                                                    |
| nbody          | 125 ms                                                                 | 130 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 168 ms                                                                 | 171 ms: 1.01x slower                                                    |
| regex_v8       | 23.9 ms                                                                | 24.6 ms: 1.03x slower                                                   |
| regex_effbot   | 2.79 ms                                                                | 2.88 ms: 1.03x slower                                                   |
| regex_dna      | 177 ms                                                                 | 187 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 28.0 us                                                                | 27.7 us: 1.01x faster                                                   |
| xml_etree_generate   | 97.1 ms                                                                | 97.4 ms: 1.00x slower                                                   |
| xml_etree_process    | 73.7 ms                                                                | 74.4 ms: 1.01x slower                                                   |
| unpickle_pure_python | 327 us                                                                 | 331 us: 1.01x slower                                                    |
| xml_etree_iterparse  | 89.6 ms                                                                | 90.6 ms: 1.01x slower                                                   |
| json_dumps           | 13.7 ms                                                                | 13.9 ms: 1.01x slower                                                   |
| tomli_loads          | 2.51 sec                                                               | 2.57 sec: 1.02x slower                                                  |
| pickle_pure_python   | 493 us                                                                 | 510 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                   |
| python_startup_no_site | 9.78 ms                                                                | 9.76 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 50.5 ms                                                                | 50.1 ms: 1.01x faster                                                   |
| mako            | 17.2 ms                                                                | 17.2 ms: 1.00x slower                                                   |
| genshi_xml      | 63.4 ms                                                                | 64.9 ms: 1.02x slower                                                   |
| genshi_text     | 30.4 ms                                                                | 31.3 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3+-bb9d955 | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                   |
| pidigits                   | 192 ms                                                                 | 182 ms: 1.05x faster                                                    |
| create_gc_cycles           | 1.84 ms                                                                | 1.81 ms: 1.02x faster                                                   |
| spectral_norm              | 113 ms                                                                 | 111 ms: 1.01x faster                                                    |
| json_loads                 | 28.0 us                                                                | 27.7 us: 1.01x faster                                                   |
| deepcopy_memo              | 40.9 us                                                                | 40.5 us: 1.01x faster                                                   |
| django_template            | 50.5 ms                                                                | 50.1 ms: 1.01x faster                                                   |
| coroutines                 | 24.6 ms                                                                | 24.4 ms: 1.01x faster                                                   |
| deepcopy                   | 326 us                                                                 | 324 us: 1.01x faster                                                    |
| shortest_path              | 553 ms                                                                 | 550 ms: 1.00x faster                                                    |
| k_core                     | 2.36 sec                                                               | 2.35 sec: 1.00x faster                                                  |
| comprehensions             | 27.7 us                                                                | 27.6 us: 1.00x faster                                                   |
| python_startup             | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                   |
| python_startup_no_site     | 9.78 ms                                                                | 9.76 ms: 1.00x faster                                                   |
| mako                       | 17.2 ms                                                                | 17.2 ms: 1.00x slower                                                   |
| xml_etree_generate         | 97.1 ms                                                                | 97.4 ms: 1.00x slower                                                   |
| bpe_tokeniser              | 5.04 sec                                                               | 5.06 sec: 1.00x slower                                                  |
| 2to3                       | 350 ms                                                                 | 352 ms: 1.00x slower                                                    |
| float                      | 108 ms                                                                 | 108 ms: 1.00x slower                                                    |
| sympy_str                  | 355 ms                                                                 | 357 ms: 1.00x slower                                                    |
| sqlglot_parse              | 2.32 ms                                                                | 2.33 ms: 1.00x slower                                                   |
| scimark_lu                 | 158 ms                                                                 | 159 ms: 1.01x slower                                                    |
| pycparser                  | 1.38 sec                                                               | 1.39 sec: 1.01x slower                                                  |
| nqueens                    | 99.4 ms                                                                | 100 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 66.5 ms                                                                | 67.0 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 3.41 us                                                                | 3.44 us: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 567 ms: 1.01x slower                                                    |
| raytrace                   | 487 ms                                                                 | 491 ms: 1.01x slower                                                    |
| meteor_contest             | 132 ms                                                                 | 133 ms: 1.01x slower                                                    |
| pyflate                    | 643 ms                                                                 | 649 ms: 1.01x slower                                                    |
| xml_etree_process          | 73.7 ms                                                                | 74.4 ms: 1.01x slower                                                   |
| scimark_sor                | 213 ms                                                                 | 215 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 5.65 ms                                                                | 5.71 ms: 1.01x slower                                                   |
| scimark_monte_carlo        | 105 ms                                                                 | 106 ms: 1.01x slower                                                    |
| scimark_fft                | 381 ms                                                                 | 385 ms: 1.01x slower                                                    |
| coverage                   | 98.8 ms                                                                | 99.7 ms: 1.01x slower                                                   |
| crypto_pyaes               | 89.8 ms                                                                | 90.8 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 327 us                                                                 | 331 us: 1.01x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                 | 134 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 89.6 ms                                                                | 90.6 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 935 ms                                                                 | 946 ms: 1.01x slower                                                    |
| json                       | 4.97 ms                                                                | 5.03 ms: 1.01x slower                                                   |
| sqlglot_transpile          | 2.67 ms                                                                | 2.70 ms: 1.01x slower                                                   |
| deltablue                  | 7.34 ms                                                                | 7.43 ms: 1.01x slower                                                   |
| generators                 | 38.2 ms                                                                | 38.7 ms: 1.01x slower                                                   |
| pprint_pformat             | 1.95 sec                                                               | 1.98 sec: 1.01x slower                                                  |
| json_dumps                 | 13.7 ms                                                                | 13.9 ms: 1.01x slower                                                   |
| regex_compile              | 168 ms                                                                 | 171 ms: 1.01x slower                                                    |
| thrift                     | 995 us                                                                 | 1.01 ms: 1.01x slower                                                   |
| fannkuch                   | 490 ms                                                                 | 497 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed    | 590 ms                                                                 | 599 ms: 1.02x slower                                                    |
| pathlib                    | 19.5 ms                                                                | 19.8 ms: 1.02x slower                                                   |
| async_tree_none            | 345 ms                                                                 | 351 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.11 us                                                                | 2.15 us: 1.02x slower                                                   |
| async_tree_none_tg         | 309 ms                                                                 | 314 ms: 1.02x slower                                                    |
| chaos                      | 93.6 ms                                                                | 95.4 ms: 1.02x slower                                                   |
| telco                      | 8.58 ms                                                                | 8.74 ms: 1.02x slower                                                   |
| mdp                        | 2.76 sec                                                               | 2.81 sec: 1.02x slower                                                  |
| async_tree_io              | 748 ms                                                                 | 764 ms: 1.02x slower                                                    |
| sympy_expand               | 581 ms                                                                 | 594 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 391 ms                                                                 | 400 ms: 1.02x slower                                                    |
| tomli_loads                | 2.51 sec                                                               | 2.57 sec: 1.02x slower                                                  |
| genshi_xml                 | 63.4 ms                                                                | 64.9 ms: 1.02x slower                                                   |
| async_tree_memoization     | 419 ms                                                                 | 429 ms: 1.02x slower                                                    |
| logging_simple             | 8.97 us                                                                | 9.18 us: 1.02x slower                                                   |
| richards_super             | 75.0 ms                                                                | 76.8 ms: 1.02x slower                                                   |
| go                         | 235 ms                                                                 | 241 ms: 1.02x slower                                                    |
| logging_format             | 10.1 us                                                                | 10.4 us: 1.03x slower                                                   |
| async_tree_io_tg           | 721 ms                                                                 | 740 ms: 1.03x slower                                                    |
| logging_silent             | 177 ns                                                                 | 182 ns: 1.03x slower                                                    |
| regex_v8                   | 23.9 ms                                                                | 24.6 ms: 1.03x slower                                                   |
| genshi_text                | 30.4 ms                                                                | 31.3 ms: 1.03x slower                                                   |
| richards                   | 66.4 ms                                                                | 68.6 ms: 1.03x slower                                                   |
| hexiom                     | 9.48 ms                                                                | 9.79 ms: 1.03x slower                                                   |
| regex_effbot               | 2.79 ms                                                                | 2.88 ms: 1.03x slower                                                   |
| pickle_pure_python         | 493 us                                                                 | 510 us: 1.04x slower                                                    |
| nbody                      | 125 ms                                                                 | 130 ms: 1.04x slower                                                    |
| regex_dna                  | 177 ms                                                                 | 187 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (18): sqlalchemy_imperative, sympy_sum, connected_components, html5lib, async_generators, docutils, bench_mp_pool, typing_runtime_protocols, xml_etree_parse, asyncio_websockets, sqlalchemy_declarative, dulwich_log, bench_thread_pool, many_optionals, sympy_integrate, subparsers, sphinx, pylint

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x