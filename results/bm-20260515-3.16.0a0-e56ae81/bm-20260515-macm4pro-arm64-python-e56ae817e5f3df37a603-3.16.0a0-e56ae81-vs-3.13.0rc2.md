# Results vs. 3.13.0rc2

- fork: python
- ref: e56ae817e5f3df37a603
- machine: darwin-arm64
- commit hash: e56ae81
- commit date: 2026-05-15
- overall geometric mean: 1.046x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 957 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 325 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 101 ms: 3.49x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| nbody          | 42.5 ms                                                        | 45.6 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 832 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 515 ms: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 56.3 ms: 1.88x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 99.5 us: 1.46x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.38x faster                                                   |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.9 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 307 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 325 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 832 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                   |
| pyflate                          | 222 ms                                                         | 189 ms: 1.18x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 853 us: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| docutils                         | 1.05 sec                                                       | 957 ms: 1.09x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.9 ms: 1.05x faster                                                   |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 633 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 939 ns: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.00x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.25 us: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 211 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 481 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.04x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.15 us: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                   |
| nbody                            | 42.5 ms                                                        | 45.6 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.94 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.7 ms: 1.14x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 39.6 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.0 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.46x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 68.8 ms: 1.85x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 101 ms: 3.49x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): sphinx, dask, spectral_norm, logging_format
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260515-3.16.0a0-e56ae81/bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x