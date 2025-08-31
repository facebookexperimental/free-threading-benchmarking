# Results vs. 3.12.6

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 260 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.91 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.1 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.2 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.3 ms: 1.00x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.8 ms: 1.15x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.9 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| tomli_loads          | 957 ms                                                   | 933 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.30 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| mako            | 4.77 ms                                                  | 4.98 ms: 1.04x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 260 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.41x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.91 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.65 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.2 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.5 ms: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.3 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 961 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.8 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| nbody                            | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.3 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.3 us: 1.10x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.54 us: 1.10x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.9 ms: 1.08x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 933 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.9 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.3 ms: 1.00x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 337 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.98 ms: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 51.3 ms: 1.07x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.30 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 963 us: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 326 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.1 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): sqlite_synth, shortest_path, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x