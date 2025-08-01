# Results vs. 3.13.0rc2

- fork: python
- ref: c419af9e277bea7dd78f
- machine: darwin-arm64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.012x faster
- HPT reliability: 68.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.04x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 262 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 260 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.3 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.7 ms: 1.01x slower                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 924 ms: 1.08x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.9 ms: 1.00x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.2 us: 1.00x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 257 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 262 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 260 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                   |
| go                               | 72.6 ms                                                        | 57.2 ms: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 51.4 ms: 1.24x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 924 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 951 us: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.47 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.9 us: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.9 ms: 1.00x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.2 us: 1.00x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 43.3 ms: 1.00x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| float                            | 31.4 ms                                                        | 31.7 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.62 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.2 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 968 ns: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.2 ms: 1.03x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.4 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.07x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.09x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 57.5 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                   |
| raytrace                         | 109 ms                                                         | 123 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.3 ms: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 51.0 ms: 1.19x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.93 ms: 1.59x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): json, xml_etree_generate
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 68.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x