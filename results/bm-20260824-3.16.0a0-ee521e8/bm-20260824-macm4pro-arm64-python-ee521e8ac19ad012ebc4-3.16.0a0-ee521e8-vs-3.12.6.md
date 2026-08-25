# Results vs. 3.12.6

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: darwin-arm64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.147x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 938 ms: 1.09x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 309 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 314 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 330 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.56 ms: 1.42x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.33x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 280 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 40.6 ms: 1.33x faster                                                   |
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.20x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.1 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 801 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.5 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.5 us: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 68.4 ms: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.11 ms: 1.14x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.06 ms: 5.11x faster                                                   |
| pylint                           | 128 ms                                                   | 56.3 ms: 2.27x faster                                                   |
| mdp                              | 1.09 sec                                                 | 517 ms: 2.11x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 309 ms: 1.60x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.60x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.72 us: 1.46x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 314 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 330 ms: 1.45x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.9 us: 1.42x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.56 ms: 1.42x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.33x faster                                                    |
| nbody                            | 54.2 ms                                                  | 40.6 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.6 ms: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 114 ms: 1.24x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 801 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 280 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.5 ms: 1.19x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.9 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| k_core                           | 1.12 sec                                                 | 981 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.69 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.10x faster                                                   |
| docutils                         | 1.02 sec                                                 | 938 ms: 1.09x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.1 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                   |
| fannkuch                         | 176 ms                                                   | 164 ms: 1.07x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.0 ms: 1.07x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.91 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 924 ns: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.5 us: 1.04x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 637 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 817 us: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 490 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 68.4 ms: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 423 us: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.11 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                   |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): thrift
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.147x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x