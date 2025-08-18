# Results vs. 3.13.0rc2

- fork: python
- ref: bc2872445b2aee4bb4e0
- machine: darwin-arm64
- commit hash: bc28724
- commit date: 2025-08-18
- overall geometric mean: 1.012x faster
- HPT reliability: 61.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.5 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 31.8 ms: 1.01x slower                                                   |
| nbody          | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 946 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.95 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 114 us: 1.28x faster                                                    |
| go                               | 72.6 ms                                                        | 57.5 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 51.4 ms: 1.24x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 946 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 947 us: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.8 ms: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.3 us: 1.01x slower                                                   |
| float                            | 31.4 ms                                                        | 31.8 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.5 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 675 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 334 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.5 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.57 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.95 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.74 us: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.9 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 325 us: 1.62x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.6 ms: 2.80x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.5 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): richards_super, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250818-3.15.0a0-bc28724/bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 61.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x