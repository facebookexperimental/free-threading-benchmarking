# Results vs. 3.13.0rc2

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.060x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.13x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.57x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.5 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.7 ms: 2.93x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 778 ms: 1.29x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.2 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 91.2 us: 1.09x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.08 ms: 1.10x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                   |
| mako            | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.13x faster                                                    |
| mdp                              | 1.06 sec                                                       | 527 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 244 ms: 1.66x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 981 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.5 us: 1.47x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                   |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.43x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 778 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                   |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.1 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| genshi_text                      | 9.97 ms                                                        | 9.08 ms: 1.10x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.5 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.2 ms: 1.09x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 91.2 us: 1.09x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 60.6 us: 1.07x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 616 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| thrift                           | 309 us                                                         | 295 us: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 397 us: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.3 ns: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.38 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 158 ms: 1.01x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 94.9 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.7 ms: 1.01x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.90 us: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.2 ms: 1.02x slower                                                   |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.4 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.4 ms: 1.04x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.1 ms: 1.05x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 358 us: 1.78x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.7 ms: 2.93x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (2): dask, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x