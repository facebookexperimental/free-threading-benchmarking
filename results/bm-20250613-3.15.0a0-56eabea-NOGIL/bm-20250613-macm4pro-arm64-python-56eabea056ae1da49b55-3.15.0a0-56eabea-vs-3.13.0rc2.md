# Results vs. 3.13.0rc2

- fork: python
- ref: 56eabea056ae1da49b55
- machine: darwin-arm64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.004x faster
- HPT reliability: 86.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 423 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 991 ms: 1.01x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.62 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.78 ms: 1.13x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.09 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 813 us: 2.51x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 496 us: 2.00x faster                                                    |
| mdp                              | 1.06 sec                                                       | 568 ms: 1.86x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| deepcopy                         | 145 us                                                         | 121 us: 1.20x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.6 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.3 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 991 ms: 1.01x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.62 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 533 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| sphinx                           | 409 ms                                                         | 423 ms: 1.04x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.07 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.4 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.6 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.78 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.4 us: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 28.1 ms: 1.14x slower                                                   |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.15x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.69 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.01 us: 1.18x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 380 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.09 ms: 1.19x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 775 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.21x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 53.2 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.82 us: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.14 us: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.5 ms: 1.29x slower                                                   |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 595 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 62.1 ms: 1.45x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.89 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 219 ns: 5.40x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 86.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x