# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.477x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 42.0 ms: 1.30x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.97 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 33.6 ms: 1.16x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.3 ms: 1.15x faster                                                   |
| tomli_loads          | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 95.0 us: 1.08x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.40 ms: 1.08x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.92 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pprint_pformat                   | 665 ms                                                   | 590 ns: 1127250.33x faster                                              |
| pprint_safe_repr                 | 328 ms                                                   | 344 ns: 952941.01x faster                                               |
| subparsers                       | 20.8 ms                                                  | 9.79 ms: 2.12x faster                                                   |
| mdp                              | 1.09 sec                                                 | 527 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 42.0 ms: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| go                               | 70.0 ms                                                  | 57.1 ms: 1.23x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.4 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 46.5 ms: 1.17x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 33.6 ms: 1.16x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.3 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.6 us: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.40 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 95.0 us: 1.08x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.92 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.62 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 942 ns: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.0 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.58 us: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 512 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.97 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                    |
| connected_components             | 201 ms                                                   | 212 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.14x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.29 ms: 1.14x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 954 us: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.2 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 198 ns: 3.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.43x faster                                                            |

Benchmark hidden because not significant (3): logging_format, crypto_pyaes, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.477x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x