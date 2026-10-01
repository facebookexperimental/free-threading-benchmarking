# Results vs. 3.12.6

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: darwin-arm64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 330 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.42 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 143 ms: 1.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 344 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.32x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.9 ms: 1.45x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                   |
| pidigits       | 161 ms                                                   | 172 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.16x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.4 ms: 1.24x faster                                                   |
| tomli_loads          | 957 ms                                                   | 794 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.55 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.05x faster                                                   |
| pylint                           | 128 ms                                                   | 56.4 ms: 2.27x faster                                                   |
| mdp                              | 1.09 sec                                                 | 512 ms: 2.13x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.56x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.65 us: 1.48x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 330 ms: 1.46x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.9 us: 1.45x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.42 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 143 ms: 1.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| go                               | 70.0 ms                                                  | 52.3 ms: 1.34x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 344 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.32x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.4 ms: 1.28x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 34.8 ms: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.4 ms: 1.24x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 794 ms: 1.21x faster                                                    |
| pyflate                          | 216 ms                                                   | 181 ms: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.17x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                   |
| fannkuch                         | 176 ms                                                   | 159 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 302 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.43 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| docutils                         | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 621 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 96.6 us: 1.07x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.2 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.55 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 308 us: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.0 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                   |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 864 us: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 172 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.0 ms: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.53 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 65.9 ms: 1.45x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (3): bench_thread_pool, gc_traversal, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x