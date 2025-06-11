# Results vs. 3.13.0rc2

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: darwin-arm64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.039x faster
- HPT reliability: 99.04%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.9 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.2 ms: 1.01x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| mdp                              | 1.06 sec                                                       | 507 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 54.9 ms: 1.32x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.3 us: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.5 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.9 ms: 1.03x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.2 ms: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 97.6 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 486 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 46.0 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.26 us: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 347 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 711 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.64 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.9 ms: 3.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.04% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x