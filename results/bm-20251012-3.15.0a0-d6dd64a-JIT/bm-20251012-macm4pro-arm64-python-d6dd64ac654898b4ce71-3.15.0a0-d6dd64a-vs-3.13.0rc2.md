# Results vs. 3.13.0rc2

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.017x faster
- HPT reliability: 85.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 825 ms: 1.21x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.6 us: 1.06x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.40 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.43x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| go                               | 72.6 ms                                                        | 57.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 825 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.69 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 291 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 592 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.6 us: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 936 us: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 937 ns: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.0 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| sympy_integrate                  | 7.53 ms                                                        | 7.59 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.88 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.8 ns: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.53 us: 1.04x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 494 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| shortest_path                    | 225 ms                                                         | 241 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.40 ms: 1.08x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.35 us: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.9 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.7 ms: 1.16x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| many_optionals                   | 200 us                                                         | 379 us: 1.89x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.87x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (8): float, typing_runtime_protocols, mako, regex_dna, sphinx, genshi_text, bench_thread_pool, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 85.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x