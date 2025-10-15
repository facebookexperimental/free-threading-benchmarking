# Results vs. 3.13.0rc2

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.037x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 871 ms: 1.15x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.3 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.73 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.44x faster                                                   |
| deepcopy                         | 145 us                                                         | 103 us: 1.40x faster                                                    |
| go                               | 72.6 ms                                                        | 53.1 ms: 1.37x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 871 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 920 us: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.0 ns: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.73 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.3 us: 1.02x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 636 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                  |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.02x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.49 us: 1.02x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 97.4 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.8 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.04x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.22 us: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.8 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 370 us: 1.85x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.85x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (2): json, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x