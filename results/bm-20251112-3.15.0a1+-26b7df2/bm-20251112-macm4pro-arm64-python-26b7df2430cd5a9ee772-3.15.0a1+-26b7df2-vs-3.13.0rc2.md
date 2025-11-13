# Results vs. 3.13.0rc2

- fork: python
- ref: 26b7df2430cd5a9ee772
- machine: darwin-arm64
- commit hash: 26b7df2
- commit date: 2025-11-12
- overall geometric mean: 1.024x faster
- HPT reliability: 81.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.0 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| xml_etree_generate  | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                    |
| json_loads          | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.28x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.27x faster                                                     |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 894 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.06x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.05x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.9 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.4 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 480 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.30 us: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.53 us: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 319 us: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 980 ns: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.4 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.47 us: 1.10x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| nbody                            | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 364 us: 1.82x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.87x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.0 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (7): async_tree_eager, html5lib, dask, unpickle_pure_python, docutils, genshi_text, hexiom
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 81.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x