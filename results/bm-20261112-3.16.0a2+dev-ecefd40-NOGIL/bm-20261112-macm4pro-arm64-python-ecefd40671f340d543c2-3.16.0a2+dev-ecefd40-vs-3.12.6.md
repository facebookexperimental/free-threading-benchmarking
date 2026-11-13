# Results vs. 3.12.6

- fork: python
- ref: ecefd40671f340d543c2
- machine: darwin-arm64
- commit hash: ecefd40
- commit date: 2026-11-12
- overall geometric mean: 1.061x faster
- HPT reliability: 88.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 128 ms: 1.12x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                       |
| sphinx         | 434 ms                                                   | 453 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                    | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 113 ms: 1.83x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 307 ms: 1.61x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 305 ms: 1.58x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 302 ms: 1.48x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 184 ms: 1.26x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 146 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 143 ms: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.19x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 300 ms: 1.11x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 273 ms: 1.28x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.40x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 116 ms: 3.60x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.2 ms: 1.14x faster                                                       |
| pidigits       | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.7 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                       |
| tomli_loads          | 957 ms                                                   | 904 ms: 1.06x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 158 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.20x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.30 ms: 4.83x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 794 us: 2.53x faster                                                        |
| pylint                           | 128 ms                                                   | 52.6 ms: 2.44x faster                                                       |
| mdp                              | 1.09 sec                                                 | 591 ms: 1.85x faster                                                        |
| async_generators                 | 206 ms                                                   | 113 ms: 1.83x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 473 us: 1.75x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 307 ms: 1.61x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 305 ms: 1.58x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 302 ms: 1.48x faster                                                        |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.8 us: 1.32x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 184 ms: 1.26x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 146 ms: 1.22x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.20x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 143 ms: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.19x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 15.3 us: 1.19x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                      |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.17x faster                                                        |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                       |
| float                            | 37.9 ms                                                  | 33.2 ms: 1.14x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                      |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 300 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.7 ms: 1.09x faster                                                       |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                       |
| pidigits                         | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                       |
| raytrace                         | 145 ms                                                   | 137 ms: 1.06x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 904 ms: 1.06x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.05x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 58.4 ms: 1.04x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.2 ns: 1.03x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                       |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                        |
| chaos                            | 28.9 ms                                                  | 28.7 ms: 1.01x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 43.2 ms: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                        |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                       |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| sympy_integrate                  | 8.02 ms                                                  | 8.18 ms: 1.02x slower                                                       |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                       |
| deltablue                        | 1.73 ms                                                  | 1.79 ms: 1.04x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                       |
| sphinx                           | 434 ms                                                   | 453 ms: 1.04x slower                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.8 ms: 1.05x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.07x slower                                                       |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                        |
| sympy_sum                        | 57.6 ms                                                  | 61.9 ms: 1.07x slower                                                       |
| thrift                           | 322 us                                                   | 346 us: 1.08x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                        |
| generators                       | 21.9 ms                                                  | 23.8 ms: 1.09x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                       |
| nbody                            | 54.2 ms                                                  | 59.7 ms: 1.10x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                       |
| 2to3                             | 114 ms                                                   | 128 ms: 1.12x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 470 us: 1.12x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 748 ms: 1.13x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 53.9 ms: 1.13x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 158 us: 1.14x slower                                                        |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 273 ms: 1.28x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.5 ms: 1.30x slower                                                       |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.40x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.1 ms: 1.53x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 116 ms: 3.60x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                                |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-ecefd40-NOGIL/bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 88.02% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x