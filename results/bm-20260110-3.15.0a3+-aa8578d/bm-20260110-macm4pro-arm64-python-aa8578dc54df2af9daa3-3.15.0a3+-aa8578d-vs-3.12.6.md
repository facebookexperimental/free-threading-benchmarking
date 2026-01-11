# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.158x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 396 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.8 ms: 1.72x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.6 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                    |
| tomli_loads          | 957 ms                                                   | 838 ms: 1.14x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.71 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.01x faster                                                     |
| mdp                              | 1.09 sec                                                 | 546 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.8 ms: 1.72x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.8 us: 1.63x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.09 us: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 53.4 ms: 1.31x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.5 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 903 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.19x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.4 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 43.9 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 838 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 396 ms: 1.09x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.71 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 304 ms: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                     |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| sqlite_synth                     | 967 ns                                                   | 975 ns: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.84 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 936 us: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.6 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): json, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.158x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x