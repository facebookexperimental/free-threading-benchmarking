# Results vs. 3.13.0rc2

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.008x faster
- HPT reliability: 62.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.9 ms: 1.08x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 259 ms: 2.02x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 261 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.7 ms: 3.10x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| float          | 31.4 ms                                                        | 32.4 ms: 1.03x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 828 ms: 1.21x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 91.8 us: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.5 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.50 ms: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.3 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 259 ms: 2.02x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 261 ms: 1.99x faster                                                    |
| mdp                              | 1.06 sec                                                       | 535 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.6 ms: 1.24x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 828 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 296 ms: 1.09x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 598 ms: 1.09x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 91.8 us: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| xml_etree_process                | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.93 ms: 1.05x faster                                                   |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.5 ms: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.50 ms: 1.03x faster                                                   |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 968 us: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.0 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.5 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                   |
| float                            | 31.4 ms                                                        | 32.4 ms: 1.03x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.79 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.04x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 22.3 ms: 1.04x slower                                                   |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 440 us: 1.07x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.04 ms: 1.07x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.9 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.6 ms: 1.08x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.3 ms: 1.08x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                    |
| pycparser                        | 470 ms                                                         | 512 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.9 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 49.0 ms: 1.12x slower                                                   |
| raytrace                         | 109 ms                                                         | 123 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.7 ms: 1.16x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.10 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 10.0 ms: 1.60x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.7 ms: 3.10x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): asyncio_websockets, async_tree_eager, json, typing_runtime_protocols, mako
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 62.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x