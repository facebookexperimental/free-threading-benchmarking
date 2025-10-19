# Results vs. 3.13.0rc2

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.015x faster
- HPT reliability: 50.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 989 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.9 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.9 ms: 2.66x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 964 ms: 1.04x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                    |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 757 us: 2.70x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 467 us: 2.13x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                     |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.9 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 995 ms: 1.47x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.26x faster                                                    |
| deepcopy                         | 145 us                                                         | 116 us: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 61.0 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 816 ns: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 989 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 964 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                     |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.08x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                     |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 716 ms: 1.10x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.74 us: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.9 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.8 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.28 us: 1.22x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.29 ms: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 542 us: 1.32x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 56.4 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 384 us: 1.92x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.9 ms: 2.66x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.9 ms: 3.01x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): sphinx, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-NOGIL/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 50.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x