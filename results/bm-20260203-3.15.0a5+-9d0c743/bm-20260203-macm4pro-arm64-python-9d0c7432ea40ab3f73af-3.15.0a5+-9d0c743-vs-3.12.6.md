# Results vs. 3.12.6

- fork: python
- ref: 9d0c7432ea40ab3f73af
- machine: darwin-arm64
- commit hash: 9d0c743
- commit date: 2026-02-03
- overall geometric mean: 1.189x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| docutils       | 1.02 sec                                                 | 981 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.7 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.91 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.1 ms: 1.26x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.8 ms: 1.22x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| tomli_loads          | 957 ms                                                   | 813 ms: 1.18x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.4 us: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.49 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.27x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| mdp                              | 1.09 sec                                                 | 526 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.7 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 95.1 us: 1.70x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.96 us: 1.41x faster                                                    |
| float                            | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.91 ms: 1.37x faster                                                    |
| go                               | 70.0 ms                                                  | 51.4 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.0 ms: 1.26x faster                                                    |
| nbody                            | 54.2 ms                                                  | 43.1 ms: 1.26x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.7 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 44.8 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.21x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.2 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 813 ms: 1.18x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 43.6 ms: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 21.7 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.2 ms: 1.17x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.4 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.16x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 61.5 us: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.23 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 450 ms: 1.10x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.49 ms: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.10x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 300 ms: 1.09x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 609 ms: 1.09x faster                                                     |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.4 us: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| fannkuch                         | 176 ms                                                   | 164 ms: 1.07x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.8 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.2 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.83 ms: 1.06x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 922 ns: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 981 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| pidigits                         | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 47.5 ms: 1.00x faster                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.77 ms: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 882 us: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.3 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260203-3.15.0a5+-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.189x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.22x