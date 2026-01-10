# Results vs. base

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 123 ms                                                                   | 121 ms: 1.02x faster                                                 |
| docutils       | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                               |
| html5lib       | 23.3 ms                                                                  | 21.2 ms: 1.10x faster                                                |
| sphinx         | 423 ms                                                                   | 417 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager              | 48.3 ms                                                                  | 41.4 ms: 1.16x faster                                                |
| async_tree_none               | 118 ms                                                                   | 110 ms: 1.07x faster                                                 |
| async_tree_io                 | 251 ms                                                                   | 239 ms: 1.05x faster                                                 |
| async_tree_memoization        | 152 ms                                                                   | 145 ms: 1.05x faster                                                 |
| async_tree_none_tg            | 108 ms                                                                   | 104 ms: 1.04x faster                                                 |
| async_tree_io_tg              | 243 ms                                                                   | 234 ms: 1.04x faster                                                 |
| async_tree_eager_io           | 250 ms                                                                   | 241 ms: 1.04x faster                                                 |
| async_tree_eager_tg           | 94.1 ms                                                                  | 91.6 ms: 1.03x faster                                                |
| async_tree_eager_memoization  | 114 ms                                                                   | 111 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed       | 270 ms                                                                   | 264 ms: 1.02x faster                                                 |
| async_tree_memoization_tg     | 145 ms                                                                   | 142 ms: 1.02x faster                                                 |
| coroutines                    | 10.7 ms                                                                  | 10.6 ms: 1.01x faster                                                |
| async_tree_eager_cpu_io_mixed | 228 ms                                                                   | 225 ms: 1.01x faster                                                 |
| async_generators              | 189 ms                                                                   | 200 ms: 1.06x slower                                                 |
| Geometric mean                | (ref)                                                                    | 1.03x faster                                                         |

Benchmark hidden because not significant (5): async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 29.0 ms                                                                  | 21.6 ms: 1.34x faster                                                |
| nbody          | 57.9 ms                                                                  | 43.7 ms: 1.33x faster                                                |
| pidigits       | 163 ms                                                                   | 165 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                    | 1.20x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 50.8 ms                                                                  | 44.3 ms: 1.15x faster                                                |
| regex_v8       | 9.20 ms                                                                  | 9.17 ms: 1.00x faster                                                |
| regex_effbot   | 1.44 ms                                                                  | 1.45 ms: 1.01x slower                                                |
| regex_dna      | 95.0 ms                                                                  | 96.0 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 110 us                                                                   | 76.8 us: 1.43x faster                                                |
| pickle_pure_python   | 147 us                                                                   | 113 us: 1.30x faster                                                 |
| tomli_loads          | 888 ms                                                                   | 739 ms: 1.20x faster                                                 |
| xml_etree_process    | 27.5 ms                                                                  | 23.5 ms: 1.17x faster                                                |
| xml_etree_generate   | 37.8 ms                                                                  | 32.3 ms: 1.17x faster                                                |
| json_dumps           | 4.05 ms                                                                  | 3.72 ms: 1.09x faster                                                |
| xml_etree_iterparse  | 39.7 ms                                                                  | 36.8 ms: 1.08x faster                                                |
| Geometric mean       | (ref)                                                                    | 1.15x faster                                                         |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.03 ms                                                                  | 7.12 ms: 1.01x slower                                                |
| python_startup         | 9.76 ms                                                                  | 9.93 ms: 1.02x slower                                                |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 5.60 ms                                                                  | 4.58 ms: 1.22x faster                                                |
| django_template | 15.9 ms                                                                  | 14.6 ms: 1.09x faster                                                |
| genshi_text     | 11.6 ms                                                                  | 11.3 ms: 1.03x faster                                                |
| genshi_xml      | 23.8 ms                                                                  | 27.4 ms: 1.16x slower                                                |
| Geometric mean  | (ref)                                                                    | 1.05x faster                                                         |

All benchmarks:
===============

| Benchmark                     | bm-20260109-macm4pro-arm64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| richards                      | 23.1 ms                                                                  | 10.4 ms: 2.23x faster                                                |
| richards_super                | 26.6 ms                                                                  | 12.6 ms: 2.11x faster                                                |
| unpickle_pure_python          | 110 us                                                                   | 76.8 us: 1.43x faster                                                |
| deltablue                     | 1.66 ms                                                                  | 1.17 ms: 1.41x faster                                                |
| scimark_lu                    | 57.5 ms                                                                  | 40.8 ms: 1.41x faster                                                |
| logging_silent                | 45.5 ns                                                                  | 32.6 ns: 1.40x faster                                                |
| float                         | 29.0 ms                                                                  | 21.6 ms: 1.34x faster                                                |
| pyflate                       | 194 ms                                                                   | 145 ms: 1.34x faster                                                 |
| nbody                         | 57.9 ms                                                                  | 43.7 ms: 1.33x faster                                                |
| scimark_monte_carlo           | 32.9 ms                                                                  | 25.0 ms: 1.32x faster                                                |
| go                            | 60.4 ms                                                                  | 46.1 ms: 1.31x faster                                                |
| pickle_pure_python            | 147 us                                                                   | 113 us: 1.30x faster                                                 |
| scimark_sor                   | 55.4 ms                                                                  | 44.5 ms: 1.25x faster                                                |
| crypto_pyaes                  | 42.5 ms                                                                  | 34.4 ms: 1.24x faster                                                |
| pprint_safe_repr              | 335 ms                                                                   | 271 ms: 1.23x faster                                                 |
| pprint_pformat                | 683 ms                                                                   | 556 ms: 1.23x faster                                                 |
| comprehensions                | 8.49 us                                                                  | 6.92 us: 1.23x faster                                                |
| mako                          | 5.60 ms                                                                  | 4.58 ms: 1.22x faster                                                |
| fannkuch                      | 174 ms                                                                   | 143 ms: 1.21x faster                                                 |
| tomli_loads                   | 888 ms                                                                   | 739 ms: 1.20x faster                                                 |
| chaos                         | 28.4 ms                                                                  | 23.9 ms: 1.19x faster                                                |
| scimark_fft                   | 128 ms                                                                   | 109 ms: 1.18x faster                                                 |
| xml_etree_process             | 27.5 ms                                                                  | 23.5 ms: 1.17x faster                                                |
| xml_etree_generate            | 37.8 ms                                                                  | 32.3 ms: 1.17x faster                                                |
| nqueens                       | 44.8 ms                                                                  | 38.4 ms: 1.17x faster                                                |
| spectral_norm                 | 51.1 ms                                                                  | 43.8 ms: 1.17x faster                                                |
| async_tree_eager              | 48.3 ms                                                                  | 41.4 ms: 1.16x faster                                                |
| hexiom                        | 3.22 ms                                                                  | 2.78 ms: 1.16x faster                                                |
| sqlglot_v2_parse              | 584 us                                                                   | 509 us: 1.15x faster                                                 |
| regex_compile                 | 50.8 ms                                                                  | 44.3 ms: 1.15x faster                                                |
| bpe_tokeniser                 | 2.03 sec                                                                 | 1.78 sec: 1.14x faster                                               |
| meteor_contest                | 56.1 ms                                                                  | 49.8 ms: 1.13x faster                                                |
| raytrace                      | 130 ms                                                                   | 117 ms: 1.11x faster                                                 |
| deepcopy_reduce               | 1.17 us                                                                  | 1.06 us: 1.11x faster                                                |
| subparsers                    | 4.18 ms                                                                  | 3.78 ms: 1.11x faster                                                |
| sqlglot_v2_transpile          | 706 us                                                                   | 641 us: 1.10x faster                                                 |
| html5lib                      | 23.3 ms                                                                  | 21.2 ms: 1.10x faster                                                |
| django_template               | 15.9 ms                                                                  | 14.6 ms: 1.09x faster                                                |
| deepcopy_memo                 | 12.8 us                                                                  | 11.7 us: 1.09x faster                                                |
| telco                         | 3.06 ms                                                                  | 2.81 ms: 1.09x faster                                                |
| deepcopy                      | 107 us                                                                   | 98.6 us: 1.09x faster                                                |
| json_dumps                    | 4.05 ms                                                                  | 3.72 ms: 1.09x faster                                                |
| xml_etree_iterparse           | 39.7 ms                                                                  | 36.8 ms: 1.08x faster                                                |
| async_tree_none               | 118 ms                                                                   | 110 ms: 1.07x faster                                                 |
| pycparser                     | 467 ms                                                                   | 436 ms: 1.07x faster                                                 |
| k_core                        | 1.00 sec                                                                 | 948 ms: 1.06x faster                                                 |
| connected_components          | 246 ms                                                                   | 233 ms: 1.06x faster                                                 |
| async_tree_io                 | 251 ms                                                                   | 239 ms: 1.05x faster                                                 |
| async_tree_memoization        | 152 ms                                                                   | 145 ms: 1.05x faster                                                 |
| logging_simple                | 2.43 us                                                                  | 2.33 us: 1.04x faster                                                |
| logging_format                | 2.69 us                                                                  | 2.58 us: 1.04x faster                                                |
| async_tree_none_tg            | 108 ms                                                                   | 104 ms: 1.04x faster                                                 |
| typing_runtime_protocols      | 71.5 us                                                                  | 68.8 us: 1.04x faster                                                |
| async_tree_io_tg              | 243 ms                                                                   | 234 ms: 1.04x faster                                                 |
| async_tree_eager_io           | 250 ms                                                                   | 241 ms: 1.04x faster                                                 |
| genshi_text                   | 11.6 ms                                                                  | 11.3 ms: 1.03x faster                                                |
| shortest_path                 | 253 ms                                                                   | 245 ms: 1.03x faster                                                 |
| async_tree_eager_tg           | 94.1 ms                                                                  | 91.6 ms: 1.03x faster                                                |
| async_tree_eager_memoization  | 114 ms                                                                   | 111 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed       | 270 ms                                                                   | 264 ms: 1.02x faster                                                 |
| async_tree_memoization_tg     | 145 ms                                                                   | 142 ms: 1.02x faster                                                 |
| 2to3                          | 123 ms                                                                   | 121 ms: 1.02x faster                                                 |
| many_optionals                | 272 us                                                                   | 267 us: 1.02x faster                                                 |
| json                          | 1.96 ms                                                                  | 1.93 ms: 1.02x faster                                                |
| sphinx                        | 423 ms                                                                   | 417 ms: 1.02x faster                                                 |
| pathlib                       | 10.8 ms                                                                  | 10.7 ms: 1.01x faster                                                |
| coroutines                    | 10.7 ms                                                                  | 10.6 ms: 1.01x faster                                                |
| async_tree_eager_cpu_io_mixed | 228 ms                                                                   | 225 ms: 1.01x faster                                                 |
| thrift                        | 338 us                                                                   | 335 us: 1.01x faster                                                 |
| docutils                      | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                               |
| generators                    | 21.1 ms                                                                  | 21.0 ms: 1.01x faster                                                |
| sqlglot_v2_normalize          | 49.4 ms                                                                  | 49.1 ms: 1.01x faster                                                |
| dulwich_log                   | 18.9 ms                                                                  | 18.8 ms: 1.00x faster                                                |
| regex_v8                      | 9.20 ms                                                                  | 9.17 ms: 1.00x faster                                                |
| coverage                      | 40.1 ms                                                                  | 40.3 ms: 1.01x slower                                                |
| sympy_integrate               | 8.12 ms                                                                  | 8.19 ms: 1.01x slower                                                |
| scimark_sparse_mat_mult       | 2.14 ms                                                                  | 2.16 ms: 1.01x slower                                                |
| regex_effbot                  | 1.44 ms                                                                  | 1.45 ms: 1.01x slower                                                |
| regex_dna                     | 95.0 ms                                                                  | 96.0 ms: 1.01x slower                                                |
| python_startup_no_site        | 7.03 ms                                                                  | 7.12 ms: 1.01x slower                                                |
| sympy_sum                     | 61.3 ms                                                                  | 62.2 ms: 1.01x slower                                                |
| bench_mp_pool                 | 46.5 ms                                                                  | 47.2 ms: 1.01x slower                                                |
| python_startup                | 9.76 ms                                                                  | 9.93 ms: 1.02x slower                                                |
| pidigits                      | 163 ms                                                                   | 165 ms: 1.02x slower                                                 |
| sympy_str                     | 111 ms                                                                   | 114 ms: 1.03x slower                                                 |
| sqlglot_v2_optimize           | 24.3 ms                                                                  | 25.5 ms: 1.05x slower                                                |
| pylint                        | 120 ms                                                                   | 126 ms: 1.05x slower                                                 |
| async_generators              | 189 ms                                                                   | 200 ms: 1.06x slower                                                 |
| mdp                           | 625 ms                                                                   | 664 ms: 1.06x slower                                                 |
| genshi_xml                    | 23.8 ms                                                                  | 27.4 ms: 1.16x slower                                                |
| Geometric mean                | (ref)                                                                    | 1.10x faster                                                         |

Benchmark hidden because not significant (13): async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, sqlite_synth, create_gc_cycles, json_loads, xml_etree_parse, sympy_expand, dask, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets, gc_traversal, bench_thread_pool

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.03x