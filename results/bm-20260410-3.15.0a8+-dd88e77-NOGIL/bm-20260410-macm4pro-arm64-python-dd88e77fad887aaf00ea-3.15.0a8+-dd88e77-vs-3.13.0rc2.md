# Results vs. 3.13.0rc2

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: darwin-arm64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.026x faster
- HPT reliability: 68.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 968 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.9 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.03 ms: 1.19x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 864 ms: 1.16x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.5 ms: 1.09x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 787 us: 2.59x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 509 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 600 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.57x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 783 ns: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.03 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 864 ms: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.5 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 968 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 452 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.4 us: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.11 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.3 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.3 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.6 ms: 1.28x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.6 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.9 ms: 1.31x slower                                                    |
| many_optionals                   | 200 us                                                         | 264 us: 1.32x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.7 ms: 1.32x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 565 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260410-3.15.0a8+-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 68.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x