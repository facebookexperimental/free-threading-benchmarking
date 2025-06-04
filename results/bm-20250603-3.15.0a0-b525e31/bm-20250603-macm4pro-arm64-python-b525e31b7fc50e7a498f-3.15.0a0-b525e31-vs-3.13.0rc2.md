# Results vs. 3.13.0rc2

- fork: python
- ref: b525e31b7fc50e7a498f
- machine: darwin-arm64
- commit hash: b525e31
- commit date: 2025-06-03
- overall geometric mean: 1.039x faster
- HPT reliability: 99.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.00x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.3 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.91 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 893 ms: 1.12x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.39 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.18x faster                                                    |
| mdp                              | 1.06 sec                                                       | 507 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                    |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 893 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.91 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 921 us: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.39 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.70 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.78 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                  |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                   |
| 2to3                             | 112 ms                                                         | 111 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 953 ns: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.2 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.15 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.9 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.49 us: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.47 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.3 ms: 2.98x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (4): sphinx, genshi_xml, xml_etree_parse, meteor_contest
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x