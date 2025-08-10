# Results vs. 3.13.0rc2

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.010x faster
- HPT reliability: 64.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 31.6 ms: 1.01x slower                                                   |
| nbody          | 42.5 ms                                                        | 51.4 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.64 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 5.07 ms: 1.15x slower                                                   |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 958 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 114 us: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 57.8 ms: 1.25x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.4 us: 1.23x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 52.8 ms: 1.21x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                   |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 936 us: 1.06x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.9 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.64 ms: 1.00x slower                                                   |
| float                            | 31.4 ms                                                        | 31.6 ms: 1.01x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.87 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 954 ns: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.1 us: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.1 ms: 1.03x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.0 ms: 1.04x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 439 us: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 504 ms: 1.07x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                   |
| fannkuch                         | 179 ms                                                         | 193 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.95 ms: 1.10x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.13x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.67 us: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.07 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.6 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.4 ms: 1.21x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 314 us: 1.56x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.75x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): richards_super, sphinx, telco, xml_etree_parse, thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 64.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x