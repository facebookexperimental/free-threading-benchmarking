# Results vs. 3.12.6

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.166x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 389 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.0 ms: 1.77x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 830 ms: 1.15x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 94.8 us: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.56 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.01 ms: 5.18x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.0 ms: 1.77x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.6 us: 1.67x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.99 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.5 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 897 ms: 1.25x faster                                                     |
| nbody                            | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 830 ms: 1.15x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.9 ms: 1.15x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.1 ms: 1.15x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.6 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.1 us: 1.12x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.7 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.9 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                     |
| sphinx                           | 434 ms                                                   | 389 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.56 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 94.8 us: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.42 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 627 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.9 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 938 ns: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.8 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.166x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x