# Results vs. 3.12.6

- fork: python
- ref: 98b4cd6fe9348ac24d5c
- machine: darwin-arm64
- commit hash: 98b4cd6
- commit date: 2025-09-02
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 411 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.5 us: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 916 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.83 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| mako            | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.63 us: 1.29x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| go                               | 70.0 ms                                                  | 57.1 ms: 1.23x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.5 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 953 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.55 us: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.94 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.3 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 411 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.5 us: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 916 ms: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.0 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.83 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 943 us: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 327 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): pycparser, pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x