# Results vs. 3.12.6

- fork: python
- ref: 910a92babf40b7b34baa
- machine: darwin-arm64
- commit hash: 910a92b
- commit date: 2026-11-16
- overall geometric mean: 1.202x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 897 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| sphinx         | 434 ms                                                   | 388 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.7 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 276 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.69 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.5 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 147 ms: 1.10x faster                                                        |
| Geometric mean | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 91.9 us: 1.12x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 63.6 ms: 1.07x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.35 ms: 1.04x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.89 ms: 5.34x faster                                                       |
| pylint                           | 128 ms                                                   | 51.4 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 503 ms: 2.17x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.7 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 276 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.7 us: 1.69x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.0 us: 1.58x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.54x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.69 us: 1.47x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.69 ms: 1.40x faster                                                       |
| float                            | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.38x faster                                                        |
| go                               | 70.0 ms                                                  | 52.1 ms: 1.34x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.0 ms: 1.33x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 108 ms: 1.31x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 635 us: 1.31x faster                                                        |
| generators                       | 21.9 ms                                                  | 16.9 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.28x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.4 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                        |
| nbody                            | 54.2 ms                                                  | 43.5 ms: 1.25x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.24x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.1 ms: 1.23x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.72 ms: 1.21x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.86 sec: 1.21x faster                                                      |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.19x faster                                                       |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 977 ms: 1.14x faster                                                        |
| docutils                         | 1.02 sec                                                 | 897 ms: 1.14x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.78 ms: 1.13x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 91.9 us: 1.12x faster                                                       |
| sphinx                           | 434 ms                                                   | 388 ms: 1.12x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.11x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.2 ms: 1.11x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| pidigits                         | 161 ms                                                   | 147 ms: 1.10x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 63.6 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                        |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                        |
| sympy_str                        | 104 ms                                                   | 98.7 ms: 1.06x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.9 ms: 1.05x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 921 ns: 1.05x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.0 ms: 1.05x faster                                                       |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                        |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                       |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.35 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.6 ms: 1.05x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                       |
| many_optionals                   | 195 us                                                   | 224 us: 1.15x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261116-3.16.0a2+dev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.202x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.15x