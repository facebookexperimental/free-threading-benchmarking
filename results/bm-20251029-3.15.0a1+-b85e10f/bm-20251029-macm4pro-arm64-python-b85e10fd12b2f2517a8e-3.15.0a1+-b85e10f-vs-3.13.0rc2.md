# Results vs. 3.13.0rc2

- fork: python
- ref: b85e10fd12b2f2517a8e
- machine: darwin-arm64
- commit hash: b85e10f
- commit date: 2025-10-29
- overall geometric mean: 1.029x faster
- HPT reliability: 94.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.29x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 50.2 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 900 ms: 1.11x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.29x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 228 ms: 2.28x faster                                                     |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 902 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 900 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.1 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.49 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 65.8 us: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 979 ns: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                    |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.0 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.47 us: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.2 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 373 us: 1.86x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.8 ms: 2.86x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (5): html5lib, json_loads, genshi_text, hexiom, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251029-3.15.0a1+-b85e10f/bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1+-b85e10f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 94.35% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x