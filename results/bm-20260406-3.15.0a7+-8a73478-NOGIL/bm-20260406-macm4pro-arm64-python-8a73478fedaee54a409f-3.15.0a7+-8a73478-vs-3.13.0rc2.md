# Results vs. 3.13.0rc2

- fork: python
- ref: 8a73478fedaee54a409f
- machine: darwin-arm64
- commit hash: 8a73478
- commit date: 2026-04-06
- overall geometric mean: 1.035x faster
- HPT reliability: 72.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.23x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.0 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 858 ms: 1.17x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 774 us: 2.64x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.23x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 492 us: 2.02x faster                                                     |
| mdp                              | 1.06 sec                                                       | 591 ms: 1.79x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.00 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 58.7 ms: 1.24x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 776 ns: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 858 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| docutils                         | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 451 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.9 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                     |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 660 ms: 1.02x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.30 us: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.54 us: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.06x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.1 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.8 ns: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.6 us: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.6 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.8 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                    |
| coverage                         | 31.2 ms                                                        | 37.6 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.22 us: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 53.4 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.8 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.32x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 565 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.0 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260406-3.15.0a7+-8a73478-NOGIL/bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 72.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x