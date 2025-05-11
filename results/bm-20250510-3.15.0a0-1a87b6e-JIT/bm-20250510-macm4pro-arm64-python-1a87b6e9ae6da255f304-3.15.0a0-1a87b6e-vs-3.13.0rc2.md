# Results vs. 3.13.0rc2

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.017x faster
- HPT reliability: 69.32%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 26.1 ms: 1.13x slower                                                   |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 101 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 865 ms: 1.16x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 94.3 us: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                   |
| json_dumps           | 4.65 ms                                                        | 5.14 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| go                               | 72.6 ms                                                        | 57.2 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.0 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 865 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 192 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 292 ms: 1.10x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 591 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 935 us: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 94.3 us: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.8 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.00x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| connected_components             | 208 ms                                                         | 212 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.6 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 66.3 us: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.03x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.74 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 101 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 504 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.14 ms: 1.10x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.3 ms: 1.11x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.1 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.4 ms: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.86 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.61 us: 1.17x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.17x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.87 us: 1.17x slower                                                   |
| nbody                            | 42.5 ms                                                        | 50.0 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.38 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 199 ns: 4.89x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (3): mako, sqlite_synth, richards_super
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 69.32% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x