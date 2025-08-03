# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.6 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.6 ms: 2.92x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 44.1 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 808 ms: 1.24x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.7 ms: 1.09x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.39 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 94.1 us: 1.06x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.11 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.2 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.3 us: 1.46x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                   |
| go                               | 72.6 ms                                                        | 50.7 ms: 1.43x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.0 ms: 1.26x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 808 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.1 ms: 1.16x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.0 ms: 1.12x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 38.6 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| genshi_xml                       | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.11 ms: 1.10x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.7 ms: 1.09x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 44.1 ms: 1.09x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.9 us: 1.06x faster                                                   |
| thrift                           | 309 us                                                         | 292 us: 1.06x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.39 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 94.1 us: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 942 us: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 622 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.4 ns: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                   |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.00x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 95.1 ms: 1.00x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 960 ns: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.99 us: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.8 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.00 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 306 us: 1.53x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 16.7 ms: 2.66x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.6 ms: 2.92x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (5): telco, dask, python_startup, pycparser, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x