# Results vs. 3.13.0rc2

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: darwin-arm64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.031x faster
- HPT reliability: 50.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 988 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.72x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.8 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 966 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.58 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.87 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.58 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.72x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 766 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 480 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| mdp                              | 1.06 sec                                                       | 570 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.8 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| go                               | 72.6 ms                                                        | 59.6 ms: 1.22x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.5 us: 1.22x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 810 ns: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| docutils                         | 1.05 sec                                                       | 988 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 966 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.58 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.20 ms: 1.04x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.99 ms: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.92 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 340 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 692 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 330 us: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.8 ns: 1.10x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.4 us: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.1 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.87 ms: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.91 us: 1.16x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.7 ms: 1.18x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.0 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.27x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.2 ms: 1.29x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 55.3 ms: 1.29x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 590 us: 1.43x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.69 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 50.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.21x