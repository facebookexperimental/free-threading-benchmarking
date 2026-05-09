# Results vs. 3.12.6

- fork: python
- ref: 354ef336e4cd48cf0c02
- machine: darwin-arm64
- commit hash: 354ef33
- commit date: 2026-05-09
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 968 ms: 1.06x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 305 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| async_generators                 | 206 ms                                                   | 147 ms: 1.40x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 331 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 277 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 258 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 45.3 ms: 1.20x faster                                                   |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.8 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 833 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.75 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.13 ms: 5.03x faster                                                   |
| pylint                           | 128 ms                                                   | 55.7 ms: 2.30x faster                                                   |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 305 ms: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| async_generators                 | 206 ms                                                   | 147 ms: 1.40x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.28 us: 1.35x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 331 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| go                               | 70.0 ms                                                  | 54.3 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.3 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.9 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.21x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.1 ns: 1.21x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 277 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.8 ms: 1.20x faster                                                   |
| nbody                            | 54.2 ms                                                  | 45.3 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 833 ms: 1.15x faster                                                    |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.75 ms: 1.13x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.30 us: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 66.5 us: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                   |
| docutils                         | 1.02 sec                                                 | 968 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 654 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 51.0 ms: 1.01x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.4 ms: 1.04x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 864 us: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.9 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 258 ms: 1.21x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 241 us: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 59.5 ms: 1.37x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (2): pidigits, xml_etree_parse
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260509-3.16.0a0-354ef33/bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.21x