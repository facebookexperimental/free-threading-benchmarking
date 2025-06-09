# Results vs. 3.13.0rc2

- fork: python
- ref: 2677dd017a033eaaad3b
- machine: darwin-arm64
- commit hash: 2677dd0
- commit date: 2025-06-08
- overall geometric mean: 1.050x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.6 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 902 ms: 1.11x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.37 ms: 1.07x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.5 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.13 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.74 ms: 1.08x slower                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 503 ms: 2.10x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.37x faster                                                   |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                    |
| go                               | 72.6 ms                                                        | 54.3 ms: 1.34x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 167 ms: 1.16x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.3 ms: 1.14x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 902 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.37 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.1 us: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.5 ms: 1.05x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.5 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.31 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 46.7 ms: 1.03x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                   |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.00x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.6 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 97.2 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 483 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.13 ms: 1.03x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.8 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.1 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.06x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.18 us: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 344 ms: 1.07x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 695 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.74 ms: 1.08x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                   |
| nbody                            | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.9 ms: 1.10x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.69 us: 1.10x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.48 us: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.4 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.37 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.6 ms: 2.96x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (2): dask, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250608-3.15.0a0-2677dd0/bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x