# Results vs. 3.13.0rc2

- fork: python
- ref: 96ef4c511f3ec763dbb0
- machine: darwin-arm64
- commit hash: 96ef4c5
- commit date: 2025-03-25
- overall geometric mean: 1.027x slower
- HPT reliability: 97.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 25.3 ms: 1.09x slower                                                    |
| sphinx         | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.43x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 204 ms: 1.99x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 89.8 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 52.6 ms: 1.22x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| float          | 31.4 ms                                                        | 32.1 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 62.1 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.59 ms: 1.01x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.09x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.8 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.16 ms: 1.11x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| json_loads           | 10.8 us                                                        | 12.2 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 161 us: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.61 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| mako            | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                    |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 766 us: 2.66x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.43x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 460 us: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 204 ms: 1.99x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 89.8 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.3 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 821 ns: 1.15x faster                                                     |
| deepcopy                         | 145 us                                                         | 128 us: 1.13x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 57.4 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| go                               | 72.6 ms                                                        | 68.1 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.8 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 15.8 us: 1.04x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.05 sec: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.59 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.32 us: 1.02x slower                                                    |
| float                            | 31.4 ms                                                        | 32.1 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.6 ms: 1.09x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 25.3 ms: 1.09x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.16 sec: 1.10x slower                                                   |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.33 ms: 1.11x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.16 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| json_loads                       | 10.8 us                                                        | 12.2 us: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                    |
| fannkuch                         | 179 ms                                                         | 204 ms: 1.14x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.52 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.4 us: 1.15x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.2 ms: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.31 ms: 1.16x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.84 ms: 1.17x slower                                                    |
| richards                         | 22.1 ms                                                        | 25.8 ms: 1.17x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.9 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.3 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 57.3 ms: 1.20x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.20x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 148 ms: 1.20x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.95 us: 1.20x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.71 us: 1.21x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 390 ms: 1.21x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 40.9 ms: 1.22x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 49.4 ns: 1.22x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 791 ms: 1.22x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 52.6 ms: 1.22x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 161 us: 1.23x slower                                                     |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| coverage                         | 31.2 ms                                                        | 39.0 ms: 1.25x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.6 ms: 1.26x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.25 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.61 ms: 1.28x slower                                                    |
| raytrace                         | 109 ms                                                         | 141 ms: 1.29x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.82 us: 1.30x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.5 ms: 1.32x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 588 us: 1.43x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.14 ms: 1.46x slower                                                    |
| nbody                            | 42.5 ms                                                        | 62.1 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                             |

Benchmark hidden because not significant (2): pathlib, tomli_loads
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250325-3.14.0a6+-96ef4c5-NOGIL/bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 97.91% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x