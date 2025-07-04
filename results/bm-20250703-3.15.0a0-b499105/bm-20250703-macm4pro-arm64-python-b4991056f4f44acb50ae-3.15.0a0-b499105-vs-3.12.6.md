# Results vs. 3.12.6

- fork: python
- ref: b4991056f4f44acb50ae
- machine: darwin-arm64
- commit hash: b499105
- commit date: 2025-07-03
- overall geometric mean: 1.087x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 415 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 260 ms: 1.84x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.7 ms: 1.09x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.1 ms: 1.00x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 46.2 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| tomli_loads          | 957 ms                                                   | 939 ms: 1.02x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.99 ms: 1.05x slower                                                   |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.81 ms: 2.12x faster                                                   |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 260 ms: 1.84x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.42x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.46 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                   |
| go                               | 70.0 ms                                                  | 57.5 ms: 1.22x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.21x faster                                                   |
| float                            | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.5 ms: 1.21x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.6 ms: 1.19x faster                                                   |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.2 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.7 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.59 ms: 1.06x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.67 us: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 415 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 939 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.6 ms: 1.01x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 99.1 ms: 1.00x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.5 ms: 1.00x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 25.5 ms: 1.01x slower                                                   |
| sqlite_synth                     | 967 ns                                                   | 977 ns: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| pycparser                        | 497 ms                                                   | 505 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 678 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.99 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.22 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 961 us: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.09 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.5 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): json, sympy_sum, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250703-3.15.0a0-b499105/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x