# Results vs. 3.12.6

- fork: python
- ref: 6c695bfad45ddde73d0d
- machine: darwin-arm64
- commit hash: 6c695bf
- commit date: 2026-10-27
- overall geometric mean: 1.212x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| docutils       | 1.02 sec                                                 | 884 ms: 1.16x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.0 ms: 1.15x faster                                                       |
| sphinx         | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.1 ms: 2.13x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 256 ms: 1.94x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 272 ms: 1.77x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 263 ms: 1.75x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.67x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 270 ms: 1.65x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.59x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 154 ms: 1.49x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.41x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.1 ms: 1.17x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.6 ms: 2.82x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.3 ms: 1.28x faster                                                       |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.98 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.48 ms: 1.22x faster                                                       |
| tomli_loads          | 957 ms                                                   | 806 ms: 1.19x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 92.3 us: 1.12x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.3 ms: 1.06x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.21 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.46 ms: 1.07x faster                                                       |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.86 ms: 5.39x faster                                                       |
| pylint                           | 128 ms                                                   | 50.1 ms: 2.56x faster                                                       |
| mdp                              | 1.09 sec                                                 | 493 ms: 2.21x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.1 ms: 2.13x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 256 ms: 1.94x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 272 ms: 1.77x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 263 ms: 1.75x faster                                                        |
| deepcopy                         | 161 us                                                   | 93.6 us: 1.73x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.67x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 270 ms: 1.65x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.59x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.1 us: 1.57x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.50 us: 1.51x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 154 ms: 1.49x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.45x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.41x faster                                                        |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                       |
| go                               | 70.0 ms                                                  | 50.7 ms: 1.38x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 609 us: 1.36x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 40.7 ms: 1.34x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.7 ms: 1.32x faster                                                       |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| nbody                            | 54.2 ms                                                  | 42.3 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 112 ms: 1.27x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.4 ms: 1.26x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 48.4 ms: 1.26x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.23x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.48 ms: 1.22x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.4 ms: 1.22x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.30 us: 1.22x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.12 us: 1.22x faster                                                       |
| pyflate                          | 216 ms                                                   | 179 ms: 1.21x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.8 ms: 1.20x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.1 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 806 ms: 1.19x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.19x faster                                                      |
| hexiom                           | 3.04 ms                                                  | 2.59 ms: 1.17x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 39.1 ms: 1.17x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.72 ms: 1.16x faster                                                       |
| docutils                         | 1.02 sec                                                 | 884 ms: 1.16x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.0 ms: 1.15x faster                                                       |
| k_core                           | 1.12 sec                                                 | 976 ms: 1.15x faster                                                        |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                       |
| sphinx                           | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 22.5 ms: 1.13x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 92.3 us: 1.12x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.21 ms: 1.11x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.1 ms: 1.08x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 11.5 ms: 1.07x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.46 ms: 1.07x faster                                                       |
| sympy_str                        | 104 ms                                                   | 97.5 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 905 ns: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 8.98 ms: 1.07x faster                                                       |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 54.3 ms: 1.06x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 64.3 ms: 1.06x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 639 ms: 1.04x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                       |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                        |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 47.9 ms: 1.00x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.21 ms: 1.02x slower                                                       |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.1 ms: 1.06x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                       |
| many_optionals                   | 195 us                                                   | 220 us: 1.13x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.6 ms: 2.82x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261027-3.16.0a1+dev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.212x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x