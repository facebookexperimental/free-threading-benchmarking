# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.074x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.8 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.6 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 838 ms: 1.19x faster                                                     |
| json_dumps          | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.71 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| mdp                              | 1.06 sec                                                       | 546 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 903 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.8 us: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 99.8 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 838 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.91 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.4 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 936 us: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 304 ms: 1.06x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.71 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.9 ms: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 975 ns: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.09 us: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.5 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.6 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (6): json, logging_format, pycparser, unpickle_pure_python, logging_silent, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x