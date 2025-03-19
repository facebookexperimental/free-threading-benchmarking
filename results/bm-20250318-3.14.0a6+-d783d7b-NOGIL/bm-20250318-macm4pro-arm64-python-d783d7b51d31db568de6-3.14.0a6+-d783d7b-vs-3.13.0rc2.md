# Results vs. 3.13.0rc2

- fork: python
- ref: d783d7b51d31db568de6
- machine: darwin-arm64
- commit hash: d783d7b
- commit date: 2025-03-18
- overall geometric mean: 1.084x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 131 ms: 1.17x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                    |
| sphinx         | 409 ms                                                         | 435 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 231 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.6 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| async_generators                 | 193 ms                                                         | 201 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 55.7 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.04x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| float          | 31.4 ms                                                        | 35.5 ms: 1.13x slower                                                    |
| nbody          | 42.5 ms                                                        | 77.5 ms: 1.82x slower                                                    |
| Geometric mean | (ref)                                                          | 1.25x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.4 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 58.5 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.23 ms: 1.12x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 40.8 ms: 1.14x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 30.2 ms: 1.19x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.28x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 170 us: 1.30x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.14 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 13.0 ms: 1.30x slower                                                    |
| mako            | 4.41 ms                                                        | 6.12 ms: 1.39x slower                                                    |
| django_template | 12.5 ms                                                        | 18.2 ms: 1.46x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.34x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 231 ms: 2.27x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 925 us: 2.21x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 503 us: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 224 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.38x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.6 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| deepcopy                         | 145 us                                                         | 128 us: 1.13x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 838 ns: 1.13x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 91.4 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| go                               | 72.6 ms                                                        | 74.4 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.5 ms: 1.04x slower                                                    |
| async_generators                 | 193 ms                                                         | 201 ms: 1.04x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                    |
| pyflate                          | 222 ms                                                         | 234 ms: 1.05x slower                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 17.4 us: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.14 ms: 1.06x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.26 sec: 1.06x slower                                                   |
| tomli_loads                      | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| sphinx                           | 409 ms                                                         | 435 ms: 1.06x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 40.5 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 504 ms: 1.07x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.39 us: 1.08x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 70.1 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.23 ms: 1.12x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.19 sec: 1.13x slower                                                   |
| float                            | 31.4 ms                                                        | 35.5 ms: 1.13x slower                                                    |
| connected_components             | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 40.8 ms: 1.14x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.14x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.8 ms: 1.14x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.85 ms: 1.17x slower                                                    |
| pylint                           | 106 ms                                                         | 124 ms: 1.17x slower                                                     |
| 2to3                             | 112 ms                                                         | 131 ms: 1.17x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.64 ms: 1.19x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 30.2 ms: 1.19x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.1 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 58.5 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.2 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 9.30 ms: 1.24x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 79.9 us: 1.24x slower                                                    |
| richards                         | 22.1 ms                                                        | 27.4 ms: 1.24x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                                    |
| fannkuch                         | 179 ms                                                         | 223 ms: 1.25x slower                                                     |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 120 ms: 1.25x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 200 ms: 1.26x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.83 us: 1.27x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.10 us: 1.27x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 410 ms: 1.27x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 31.5 ms: 1.28x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.28x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 836 ms: 1.29x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 55.7 ms: 1.29x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 13.0 ms: 1.30x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 170 us: 1.30x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 49.4 ms: 1.33x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 164 ms: 1.33x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.2 ms: 1.34x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 59.0 ms: 1.35x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 55.3 ns: 1.36x slower                                                    |
| chaos                            | 24.3 ms                                                        | 33.5 ms: 1.38x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.01 ms: 1.38x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 46.5 ms: 1.38x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.95 ms: 1.39x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.12 ms: 1.39x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.9 ms: 1.39x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.55 ms: 1.43x slower                                                    |
| raytrace                         | 109 ms                                                         | 158 ms: 1.45x slower                                                     |
| django_template                  | 12.5 ms                                                        | 18.2 ms: 1.46x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 612 us: 1.49x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 10.1 us: 1.49x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.36 ms: 1.49x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 65.0 ms: 1.52x slower                                                    |
| nbody                            | 42.5 ms                                                        | 77.5 ms: 1.82x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.04x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x slower                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250318-3.14.0a6+-d783d7b-NOGIL/bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.17x