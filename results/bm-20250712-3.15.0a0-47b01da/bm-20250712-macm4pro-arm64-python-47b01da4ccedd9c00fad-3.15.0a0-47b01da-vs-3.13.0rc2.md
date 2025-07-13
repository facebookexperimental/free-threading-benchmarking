# Results vs. 3.13.0rc2

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.022x faster
- HPT reliability: 61.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.9 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 939 ms: 1.06x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.52 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.00x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.2 ms: 1.06x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 5.00 ms: 1.13x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 516 ms: 2.05x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 57.3 ms: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 939 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.52 ms: 1.03x faster                                                   |
| float                            | 31.4 ms                                                        | 30.6 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 969 us: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 22.0 ms: 1.00x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.5 ms: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 970 ns: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 66.2 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.30 us: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.00 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.1 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.81 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.9 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (6): thrift, fannkuch, genshi_text, logging_silent, sympy_integrate, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 61.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x