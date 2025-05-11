# Results vs. 3.13.0rc2

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.063x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.9 ms: 2.93x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.53 ms: 1.05x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 805 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.2 ms: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.47 ms: 1.02x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.07 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.7 ms: 1.09x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.48 ms: 1.05x faster                                                   |
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 14.2 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 952 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.3 us: 1.46x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                   |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.42x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.4 ms: 1.24x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 805 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.1 ms: 1.16x faster                                                   |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.1 ms: 1.11x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.56 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.7 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 33.2 ms: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.06x faster                                                    |
| thrift                           | 309 us                                                         | 291 us: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.53 ms: 1.05x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.48 ms: 1.05x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.40 ms: 1.03x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.47 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 937 ns: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 94.8 ms: 1.01x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.6 ms: 1.01x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 52.8 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.07 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 421 us: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.25 us: 1.07x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.98 ms: 1.11x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.8 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.2 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.6 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.00 ms: 1.44x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.9 ms: 2.93x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 194 ns: 4.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (3): sphinx, pycparser, docutils
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-CLANG/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x