# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: jit_inline_funcptr
- machine: darwin-arm64
- commit hash: e4a2fff
- commit date: 2026-04-03
- overall geometric mean: 1.189x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                           |
| docutils       | 1.05 sec                                                       | 971 ms: 1.08x faster                                                           |
| html5lib       | 23.1 ms                                                        | 19.3 ms: 1.20x faster                                                          |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                           |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                           |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                           |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.90x faster                                                           |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                           |
| async_tree_none                  | 142 ms                                                         | 89.9 ms: 1.58x faster                                                          |
| async_tree_none_tg               | 133 ms                                                         | 89.3 ms: 1.49x faster                                                          |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.45x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                           |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                           |
| async_tree_eager                 | 43.2 ms                                                        | 36.6 ms: 1.18x faster                                                          |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                           |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                           |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                           |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                          |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                           |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                           |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.68x slower                                                          |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                          |
| nbody          | 42.5 ms                                                        | 34.0 ms: 1.25x faster                                                          |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                          | 1.20x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.9 ms: 1.20x faster                                                          |
| regex_v8       | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                          |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                          |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 633 ms: 1.58x faster                                                           |
| json_dumps           | 4.65 ms                                                        | 3.52 ms: 1.32x faster                                                          |
| xml_etree_process    | 25.4 ms                                                        | 21.1 ms: 1.20x faster                                                          |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                          |
| unpickle_pure_python | 99.5 us                                                        | 84.5 us: 1.18x faster                                                          |
| xml_etree_generate   | 35.8 ms                                                        | 31.8 ms: 1.13x faster                                                          |
| pickle_pure_python   | 130 us                                                         | 125 us: 1.04x faster                                                           |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                          |
| xml_etree_parse      | 62.4 ms                                                        | 64.6 ms: 1.04x slower                                                          |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                          |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                          |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 8.93 ms: 1.12x faster                                                          |
| mako            | 4.41 ms                                                        | 4.10 ms: 1.08x faster                                                          |
| genshi_xml      | 21.4 ms                                                        | 20.3 ms: 1.05x faster                                                          |
| django_template | 12.5 ms                                                        | 12.4 ms: 1.01x faster                                                          |
| Geometric mean  | (ref)                                                          | 1.06x faster                                                                   |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                           |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                           |
| richards                         | 22.1 ms                                                        | 9.74 ms: 2.27x faster                                                          |
| richards_super                   | 24.7 ms                                                        | 11.6 ms: 2.12x faster                                                          |
| mdp                              | 1.06 sec                                                       | 520 ms: 2.03x faster                                                           |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.90x faster                                                           |
| scimark_sor                      | 64.0 ms                                                        | 34.7 ms: 1.85x faster                                                          |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                           |
| subparsers                       | 6.26 ms                                                        | 3.54 ms: 1.77x faster                                                          |
| k_core                           | 1.46 sec                                                       | 859 ms: 1.70x faster                                                           |
| async_tree_none                  | 142 ms                                                         | 89.9 ms: 1.58x faster                                                          |
| tomli_loads                      | 1000 ms                                                        | 633 ms: 1.58x faster                                                           |
| go                               | 72.6 ms                                                        | 46.7 ms: 1.55x faster                                                          |
| scimark_lu                       | 42.8 ms                                                        | 27.8 ms: 1.54x faster                                                          |
| deepcopy                         | 145 us                                                         | 94.5 us: 1.53x faster                                                          |
| deepcopy_memo                    | 16.5 us                                                        | 10.9 us: 1.50x faster                                                          |
| pyflate                          | 222 ms                                                         | 148 ms: 1.50x faster                                                           |
| async_tree_none_tg               | 133 ms                                                         | 89.3 ms: 1.49x faster                                                          |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.45x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                           |
| float                            | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                          |
| json_dumps                       | 4.65 ms                                                        | 3.52 ms: 1.32x faster                                                          |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.31x faster                                                          |
| scimark_fft                      | 124 ms                                                         | 94.4 ms: 1.31x faster                                                          |
| pprint_safe_repr                 | 322 ms                                                         | 247 ms: 1.30x faster                                                           |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.9 ms: 1.30x faster                                                          |
| pprint_pformat                   | 650 ms                                                         | 500 ms: 1.30x faster                                                           |
| logging_format                   | 2.45 us                                                        | 1.90 us: 1.29x faster                                                          |
| logging_simple                   | 2.24 us                                                        | 1.74 us: 1.28x faster                                                          |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.28x faster                                                          |
| nbody                            | 42.5 ms                                                        | 34.0 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                           |
| logging_silent                   | 40.6 ns                                                        | 33.6 ns: 1.21x faster                                                          |
| html5lib                         | 23.1 ms                                                        | 19.3 ms: 1.20x faster                                                          |
| regex_compile                    | 47.9 ms                                                        | 39.9 ms: 1.20x faster                                                          |
| xml_etree_process                | 25.4 ms                                                        | 21.1 ms: 1.20x faster                                                          |
| spectral_norm                    | 43.7 ms                                                        | 36.5 ms: 1.20x faster                                                          |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                          |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.79 sec: 1.19x faster                                                         |
| fannkuch                         | 179 ms                                                         | 151 ms: 1.18x faster                                                           |
| chaos                            | 24.3 ms                                                        | 20.5 ms: 1.18x faster                                                          |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                          |
| hexiom                           | 2.85 ms                                                        | 2.41 ms: 1.18x faster                                                          |
| async_tree_eager                 | 43.2 ms                                                        | 36.6 ms: 1.18x faster                                                          |
| unpickle_pure_python             | 99.5 us                                                        | 84.5 us: 1.18x faster                                                          |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                           |
| nqueens                          | 37.2 ms                                                        | 31.9 ms: 1.17x faster                                                          |
| comprehensions                   | 6.80 us                                                        | 5.87 us: 1.16x faster                                                          |
| xml_etree_generate               | 35.8 ms                                                        | 31.8 ms: 1.13x faster                                                          |
| genshi_text                      | 9.97 ms                                                        | 8.93 ms: 1.12x faster                                                          |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                          |
| regex_v8                         | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                          |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                          |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                           |
| docutils                         | 1.05 sec                                                       | 971 ms: 1.08x faster                                                           |
| mako                             | 4.41 ms                                                        | 4.10 ms: 1.08x faster                                                          |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                          |
| crypto_pyaes                     | 33.6 ms                                                        | 31.6 ms: 1.07x faster                                                          |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                           |
| pycparser                        | 470 ms                                                         | 445 ms: 1.06x faster                                                           |
| genshi_xml                       | 21.4 ms                                                        | 20.3 ms: 1.05x faster                                                          |
| create_gc_cycles                 | 993 us                                                         | 943 us: 1.05x faster                                                           |
| meteor_contest                   | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                                          |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                          |
| shortest_path                    | 225 ms                                                         | 214 ms: 1.05x faster                                                           |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                           |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.70 ms: 1.04x faster                                                          |
| pickle_pure_python               | 130 us                                                         | 125 us: 1.04x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                           |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                          |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                           |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                           |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                          |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                           |
| sqlite_synth                     | 948 ns                                                         | 939 ns: 1.01x faster                                                           |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                           |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                          |
| django_template                  | 12.5 ms                                                        | 12.4 ms: 1.01x faster                                                          |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                           |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                          |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                          |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                          |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                          |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                           |
| sympy_str                        | 95.5 ms                                                        | 98.5 ms: 1.03x slower                                                          |
| xml_etree_parse                  | 62.4 ms                                                        | 64.6 ms: 1.04x slower                                                          |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                           |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                          |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                           |
| coverage                         | 31.2 ms                                                        | 34.2 ms: 1.10x slower                                                          |
| many_optionals                   | 200 us                                                         | 225 us: 1.12x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                           |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                           |
| gc_traversal                     | 2.04 ms                                                        | 2.38 ms: 1.17x slower                                                          |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                          |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                          |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.68x slower                                                          |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                                   |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260403-3.15.0a7+-e4a2fff-JIT/bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.189x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x