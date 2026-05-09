# Results vs. 3.12.6

- fork: python
- ref: 354ef336e4cd48cf0c02
- machine: darwin-arm64
- commit hash: 354ef33
- commit date: 2026-05-09
- overall geometric mean: 1.095x faster
- HPT reliability: 99.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 441 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 283 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.60x faster                                                    |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 131 ms: 1.31x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 284 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 292 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 107 ms: 3.34x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.9 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                   |
| tomli_loads          | 957 ms                                                   | 876 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.28 ms: 4.85x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 798 us: 2.52x faster                                                    |
| pylint                           | 128 ms                                                   | 53.4 ms: 2.40x faster                                                   |
| mdp                              | 1.09 sec                                                 | 584 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 283 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 514 us: 1.61x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.60x faster                                                    |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.39x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 131 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 795 ns: 1.22x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.18 us: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 284 ms: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 58.8 ms: 1.19x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 43.4 ns: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| float                            | 37.9 ms                                                  | 32.9 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 292 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 876 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 56.6 ms: 1.08x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 50.6 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.8 ms: 1.07x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.5 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.70 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.00 ms: 1.00x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx                           | 434 ms                                                   | 441 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.5 us: 1.04x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.0 ms: 1.13x slower                                                   |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.9 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.16x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 61.6 ms: 1.20x slower                                                   |
| connected_components             | 201 ms                                                   | 242 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 263 us: 1.35x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 107 ms: 3.34x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): dask, async_tree_eager, json_loads
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260509-3.16.0a0-354ef33-NOGIL/bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 99.72% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x