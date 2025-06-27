# Results vs. 3.13.0rc2

- fork: python
- ref: 34ce1920ca33c11ca2c3
- machine: darwin-arm64
- commit hash: 34ce192
- commit date: 2025-06-26
- overall geometric mean: 1.017x faster
- HPT reliability: 53.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 258 ms: 1.57x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.4 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.8 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 935 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.16 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.3 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 258 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                   |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.4 ms: 1.25x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 935 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 957 us: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.03x faster                                                   |
| float                            | 31.4 ms                                                        | 30.8 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.8 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.9 ns: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.16 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.3 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 676 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.3 ms: 1.04x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 437 us: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 501 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.08x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.43 us: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.53 us: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| raytrace                         | 109 ms                                                         | 123 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.7 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.74 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.4 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): json_loads, thrift, async_tree_eager_cpu_io_mixed, richards, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 53.70% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x