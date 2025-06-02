# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.085x faster
- HPT reliability: 94.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 994 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 797 us: 2.52x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.87 ms: 2.10x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                   |
| mdp                              | 1.09 sec                                                 | 566 ms: 1.93x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 497 us: 1.67x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| deepcopy                         | 161 us                                                   | 122 us: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.00 us: 1.23x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 62.1 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 56.1 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.3 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.05 ms: 1.00x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.09 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 994 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.6 ms: 1.10x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.0 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.85 us: 1.11x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.16 us: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.7 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 384 ms: 1.17x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 780 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.3 ms: 1.25x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.32 ms: 1.27x slower                                                   |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 593 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.46x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 219 ns: 4.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (2): scimark_fft, async_tree_eager_memoization_tg
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 94.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x