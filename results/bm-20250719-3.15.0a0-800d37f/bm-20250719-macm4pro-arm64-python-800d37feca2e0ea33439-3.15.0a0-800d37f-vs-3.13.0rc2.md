# Results vs. 3.13.0rc2

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.008x faster
- HPT reliability: 76.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.03x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.4 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.9 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 949 ms: 1.05x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.45 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.9 ms: 1.00x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.0 ms: 1.06x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                   |
| mako            | 4.41 ms                                                        | 5.01 ms: 1.13x slower                                                   |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 524 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.58x faster                                                    |
| k_core                           | 1.46 sec                                                       | 962 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.28x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 51.2 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 58.8 ms: 1.23x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 949 ms: 1.05x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.45 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 978 us: 1.02x faster                                                    |
| float                            | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.9 ms: 1.00x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.1 us: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.0 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.63 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 970 ns: 1.02x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.03x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.7 ms: 1.04x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.9 ms: 1.06x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.3 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 340 ms: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.0 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.5 ms: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 506 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.57 ms: 1.08x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.09x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 57.5 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.50 us: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.01 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.4 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.4 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.20x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 51.2 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.99 ms: 1.60x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): json, telco, richards, xml_etree_generate, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 76.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x