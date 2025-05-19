# Results vs. 3.13.0rc2

- fork: python
- ref: 9983c7d4416cac8deb2f
- machine: darwin-arm64
- commit hash: 9983c7d
- commit date: 2025-05-18
- overall geometric mean: 1.028x faster
- HPT reliability: 90.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.0 ms: 2.97x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 963 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.8 us: 1.00x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): json_dumps, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.52 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 922 us: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 199 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 963 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.8 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.7 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.52 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.8 us: 1.00x slower                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 656 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.8 us: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 435 us: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.4 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.99 ms: 1.12x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.65 us: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.53 us: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.4 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.57 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.0 ms: 2.97x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (8): pprint_safe_repr, json_dumps, sqlite_synth, fannkuch, pathlib, sphinx, json, xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250518-3.15.0a0-9983c7d/bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 90.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x