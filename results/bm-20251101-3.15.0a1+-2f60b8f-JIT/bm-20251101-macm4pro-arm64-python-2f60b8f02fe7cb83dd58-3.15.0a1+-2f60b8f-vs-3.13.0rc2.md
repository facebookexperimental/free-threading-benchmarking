# Results vs. 3.13.0rc2

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.024x faster
- HPT reliability: 92.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 54.1 ms: 1.27x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 94.2 us: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| mdp                              | 1.06 sec                                                       | 556 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 933 ms: 1.57x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| go                               | 72.6 ms                                                        | 57.7 ms: 1.26x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 288 ms: 1.12x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.74 ms: 1.12x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 584 ms: 1.11x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 94.2 us: 1.06x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| float                            | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.5 us: 1.03x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.77 ms: 1.03x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.95 ms: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 320 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 488 ms: 1.04x slower                                                     |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| shortest_path                    | 225 ms                                                         | 237 ms: 1.05x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 105 ms: 1.10x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.7 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.11x slower                                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.4 ms: 1.11x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.12x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.00 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.7 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.2 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 50.6 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 54.1 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 367 us: 1.83x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.9 ms: 2.85x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (7): mako, sphinx, docutils, dask, async_tree_eager, fannkuch, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 92.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x