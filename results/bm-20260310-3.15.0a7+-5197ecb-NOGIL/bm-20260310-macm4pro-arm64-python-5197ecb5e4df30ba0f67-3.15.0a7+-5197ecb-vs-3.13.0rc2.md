# Results vs. 3.13.0rc2

- fork: python
- ref: 5197ecb5e4df30ba0f67
- machine: darwin-arm64
- commit hash: 5197ecb
- commit date: 2026-03-10
- overall geometric mean: 1.024x faster
- HPT reliability: 59.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 998 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 419 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.6 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 844 ms: 1.18x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.96 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 813 us: 2.51x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 507 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 844 ms: 1.18x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 802 ns: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.7 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 998 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 419 ms: 1.03x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 672 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.8 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.08x slower                                                     |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.4 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.96 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.37 us: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.8 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.0 ms: 1.29x slower                                                    |
| many_optionals                   | 200 us                                                         | 263 us: 1.31x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.0 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.6 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260310-3.15.0a7+-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 59.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x