# Results vs. 3.13.0rc2

- fork: python
- ref: 180b3eb697bf5bb0088f
- machine: darwin-arm64
- commit hash: 180b3eb
- commit date: 2025-07-16
- overall geometric mean: 1.022x faster
- HPT reliability: 79.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.9 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 905 ms: 1.10x faster                                                    |
| json_dumps          | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| xml_etree_iterparse | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| json_loads          | 10.8 us                                                        | 10.8 us: 1.01x faster                                                   |
| xml_etree_process   | 25.4 ms                                                        | 25.4 ms: 1.00x slower                                                   |
| xml_etree_parse     | 62.4 ms                                                        | 64.7 ms: 1.04x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.59 ms: 1.00x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 56.3 ms: 1.29x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 905 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 938 us: 1.06x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.8 us: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.59 ms: 1.00x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.51 ms: 1.00x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.4 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 969 ns: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.2 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.8 ns: 1.03x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.1 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.04x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.7 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.8 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 439 us: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.4 ms: 1.07x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.9 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.5 ms: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.92 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (6): typing_runtime_protocols, float, async_tree_eager_cpu_io_mixed, sphinx, unpickle_pure_python, genshi_text
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 79.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x