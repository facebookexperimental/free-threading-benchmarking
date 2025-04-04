# Results vs. 3.13.0rc2

- fork: python
- ref: 96ef4c511f3ec763dbb0
- machine: darwin-arm64
- commit hash: 96ef4c5
- commit date: 2025-03-25
- overall geometric mean: 1.011x slower
- HPT reliability: 95.09%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                    |
| sphinx         | 409 ms                                                         | 419 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 261 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 135 ms: 1.31x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.0 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| float          | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.2 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 936 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.8 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.08 ms: 1.09x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.04 ms: 1.05x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 261 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                     |
| k_core                           | 1.46 sec                                                       | 963 ms: 1.52x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 114 us: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 53.2 ms: 1.20x faster                                                    |
| go                               | 72.6 ms                                                        | 61.9 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 904 us: 1.10x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 936 ms: 1.07x faster                                                     |
| pyflate                          | 222 ms                                                         | 210 ms: 1.06x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.04x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.8 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.4 us: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                     |
| float                            | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.13 ms: 1.02x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.08 sec: 1.02x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.5 ms: 1.02x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.03x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.77 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.9 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 2.96 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.04 ms: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 681 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.6 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 46.9 ms: 1.07x slower                                                    |
| fannkuch                         | 179 ms                                                         | 192 ms: 1.07x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.44 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.08 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.2 ms: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.10x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.72 us: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.00 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.77 us: 1.14x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.7 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                     |
| nbody                            | 42.5 ms                                                        | 51.2 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 135 ms: 1.31x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.04 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.0 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250325-3.14.0a6+-96ef4c5/bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 95.09% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x