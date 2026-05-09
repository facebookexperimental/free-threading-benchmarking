# Results vs. 3.13.0rc2

- fork: python
- ref: 354ef336e4cd48cf0c02
- machine: darwin-arm64
- commit hash: 354ef33
- commit date: 2026-05-09
- overall geometric mean: 1.011x faster
- HPT reliability: 66.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 441 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 283 ms: 1.85x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                    |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| float          | 31.4 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 876 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.26x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 798 us: 2.56x faster                                                    |
| pylint                           | 106 ms                                                         | 53.4 ms: 1.98x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 514 us: 1.93x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 283 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 584 ms: 1.81x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.28 ms: 1.46x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                    |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                    |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                   |
| go                               | 72.6 ms                                                        | 58.8 ms: 1.23x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 795 ns: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 191 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 876 ms: 1.14x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.6 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 284 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                    |
| float                            | 31.4 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 688 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 43.4 ns: 1.07x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| sphinx                           | 409 ms                                                         | 441 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.8 ms: 1.10x slower                                                   |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.8 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.5 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.6 ms: 1.16x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                                    |
| connected_components             | 208 ms                                                         | 242 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.70 ms: 1.17x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.18 us: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                   |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.0 ms: 1.31x slower                                                   |
| many_optionals                   | 200 us                                                         | 263 us: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.38x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.6 ms: 1.44x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_cpu_io_mixed
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260509-3.16.0a0-354ef33-NOGIL/bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 66.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x