# Results vs. 3.12.6

- fork: python
- ref: f1a47e79fb7081d3cde6
- machine: darwin-arm64
- commit hash: f1a47e7
- commit date: 2026-05-14
- overall geometric mean: 1.158x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                   |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 323 ms: 1.48x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 123 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 330 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 173 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 276 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 149 ms: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 100 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.6 ms: 1.21x faster                                                   |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.3 us: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.08 ms: 5.08x faster                                                   |
| pylint                           | 128 ms                                                   | 55.6 ms: 2.30x faster                                                   |
| mdp                              | 1.09 sec                                                 | 504 ms: 2.16x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.3 us: 1.66x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 323 ms: 1.48x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.1 us: 1.48x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.85 us: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 123 ms: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 51.6 ms: 1.36x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 330 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 173 ms: 1.28x faster                                                    |
| nbody                            | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.24x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 35.2 ms: 1.23x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.6 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 276 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                   |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                   |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.9 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| scimark_lu                       | 51.3 ms                                                  | 46.5 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.29 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| docutils                         | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.3 us: 1.07x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.0 ms: 1.07x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 624 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.0 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 476 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 931 ns: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.04x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                                   |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 850 us: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                   |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 239 us: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 149 ms: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 100 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, crypto_pyaes, sympy_expand
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.158x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x