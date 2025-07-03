# Results vs. 3.13.0rc2

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: darwin-arm64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.008x faster
- HPT reliability: 85.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.5 ms: 1.17x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 101 ms: 1.07x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.6 ms: 1.26x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.84 ms: 1.14x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.10 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 805 us: 2.53x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 502 us: 1.98x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| mdp                              | 1.06 sec                                                       | 589 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 88.0 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.6 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.19x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 62.2 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 823 ns: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                   |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 101 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.07 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.10 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.4 ns: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 712 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                   |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.84 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.5 ms: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.18x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.08 us: 1.19x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.10 ms: 1.19x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.92 us: 1.19x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 148 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.26x slower                                                   |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.9 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.84 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): pathlib, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 85.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x