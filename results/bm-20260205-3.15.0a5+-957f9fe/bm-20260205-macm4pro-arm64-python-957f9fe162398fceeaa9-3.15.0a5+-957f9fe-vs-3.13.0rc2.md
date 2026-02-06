# Results vs. 3.13.0rc2

- fork: python
- ref: 957f9fe162398fceeaa9
- machine: darwin-arm64
- commit hash: 957f9fe
- commit date: 2026-02-05
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 983 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 223 ms: 1.73x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.1 ms: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.82 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.6 ms: 1.06x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.2 us: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.43 ms: 1.06x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                     |
| mdp                              | 1.06 sec                                                       | 525 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 223 ms: 1.73x faster                                                     |
| k_core                           | 1.46 sec                                                       | 892 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                    |
| deepcopy                         | 145 us                                                         | 95.4 us: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 51.4 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.1 ms: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.3 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.7 ms: 1.14x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 883 us: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.77 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.82 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.3 ms: 1.09x faster                                                    |
| sphinx                           | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| fannkuch                         | 179 ms                                                         | 166 ms: 1.07x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 983 ms: 1.07x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 33.6 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 612 ms: 1.06x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.43 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.3 us: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                     |
| pycparser                        | 470 ms                                                         | 448 ms: 1.05x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                    |
| thrift                           | 309 us                                                         | 296 us: 1.04x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.24 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 96.2 us: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 918 ns: 1.03x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.6 ns: 1.02x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                    |
| coverage                         | 31.2 ms                                                        | 31.5 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.7 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.93 us: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.7 ms: 1.02x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.1 ms: 1.03x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.05x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.06x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (4): shortest_path, connected_components, python_startup, scimark_sparse_mat_mult
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260205-3.15.0a5+-957f9fe/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x