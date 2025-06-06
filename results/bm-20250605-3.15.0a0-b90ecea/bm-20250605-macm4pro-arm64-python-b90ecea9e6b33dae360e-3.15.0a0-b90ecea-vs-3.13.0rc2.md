# Results vs. 3.13.0rc2

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: darwin-arm64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.034x faster
- HPT reliability: 98.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.1 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 917 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.59 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| mdp                              | 1.06 sec                                                       | 512 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                   |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| go                               | 72.6 ms                                                        | 55.0 ms: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 917 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 935 us: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.6 us: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| python_startup                   | 8.63 ms                                                        | 8.59 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 965 ns: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.1 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 46.0 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.19 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.32 us: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.1 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.7 ms: 1.11x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.58 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (3): scimark_monte_carlo, sphinx, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 98.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x