# Results vs. 3.12.6

- fork: python
- ref: 7f371ed84ba471bb1b11
- machine: darwin-arm64
- commit hash: 7f371ed
- commit date: 2025-10-16
- overall geometric mean: 1.086x faster
- HPT reliability: 96.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.4 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.45 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 967 ms: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.09x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.3 ms: 1.11x slower                                                    |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| mako            | 4.77 ms                                                  | 5.83 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 767 us: 2.62x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.4 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 605 ms: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 477 us: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.37 us: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.8 ns: 1.14x faster                                                    |
| go                               | 70.0 ms                                                  | 61.7 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                     |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                     |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.45 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.00x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 967 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.6 us: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                     |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.7 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.2 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 355 ms: 1.08x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.09x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 724 ms: 1.09x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.09x slower                                                     |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.3 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.4 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.83 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 535 us: 1.28x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                    |
| many_optionals                   | 195 us                                                   | 385 us: 1.97x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251016-3.15.0a1+-7f371ed-NOGIL/bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 96.91% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x