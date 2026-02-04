# Results vs. 3.12.6

- fork: python
- ref: 9d0c7432ea40ab3f73af
- machine: darwin-arm64
- commit hash: 9d0c743
- commit date: 2026-02-03
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 960 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 232 ms: 1.92x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.1 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.7 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| nbody          | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.0 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 8.94 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                    |
| tomli_loads          | 957 ms                                                   | 835 ms: 1.15x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| mako            | 4.77 ms                                                  | 5.34 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.27x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 763 us: 2.63x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 232 ms: 1.92x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.89x faster                                                     |
| mdp                              | 1.09 sec                                                 | 589 ms: 1.85x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 779 ns: 1.24x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.00 us: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| go                               | 70.0 ms                                                  | 57.9 ms: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.6 ns: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| raytrace                         | 145 ms                                                   | 124 ms: 1.16x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 835 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 189 ms: 1.15x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.1 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| pycparser                        | 497 ms                                                   | 445 ms: 1.12x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.0 ms: 1.09x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 8.94 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| docutils                         | 1.02 sec                                                 | 960 ms: 1.06x faster                                                     |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                    |
| pidigits                         | 161 ms                                                   | 156 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 69.3 us: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.84 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.8 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.1 ms: 1.01x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.03 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 663 ms: 1.00x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.01x slower                                                    |
| thrift                           | 322 us                                                   | 325 us: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| nbody                            | 54.2 ms                                                  | 54.9 ms: 1.01x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 58.9 ms: 1.02x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 182 ms: 1.09x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 52.6 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.34 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.1 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 549 us: 1.31x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.0 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.7 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (3): dask, 2to3, genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260203-3.15.0a5+-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.36x