# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e5e9e6
- commit date: 2025-12-31
- overall geometric mean: 1.136x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| html5lib       | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                 |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.43x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.89x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 97.2 ms: 1.47x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 94.9 ms: 1.40x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                         |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.1 ms: 1.30x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                        |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                          | 1.12x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.3 ms: 1.19x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.6 us: 1.37x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 798 ms: 1.25x faster                                                         |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 114 us: 1.14x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.12 ms: 1.07x faster                                                        |
| genshi_text     | 9.97 ms                                                        | 9.58 ms: 1.04x faster                                                        |
| django_template | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.43x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                         |
| richards                         | 22.1 ms                                                        | 11.6 ms: 1.90x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.89x faster                                                         |
| richards_super                   | 24.7 ms                                                        | 13.4 ms: 1.84x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                         |
| k_core                           | 1.46 sec                                                       | 864 ms: 1.69x faster                                                         |
| scimark_sor                      | 64.0 ms                                                        | 38.2 ms: 1.68x faster                                                        |
| mdp                              | 1.06 sec                                                       | 632 ms: 1.67x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.90 ms: 1.61x faster                                                        |
| go                               | 72.6 ms                                                        | 46.3 ms: 1.57x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 97.2 ms: 1.47x faster                                                        |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                         |
| pyflate                          | 222 ms                                                         | 155 ms: 1.43x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 94.9 ms: 1.40x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 72.6 us: 1.37x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                         |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.0 ms: 1.30x faster                                                        |
| float                            | 31.4 ms                                                        | 24.1 ms: 1.30x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.28x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 798 ms: 1.25x faster                                                         |
| deltablue                        | 1.45 ms                                                        | 1.17 ms: 1.24x faster                                                        |
| scimark_lu                       | 42.8 ms                                                        | 34.6 ms: 1.23x faster                                                        |
| logging_format                   | 2.45 us                                                        | 1.98 us: 1.23x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.81 us: 1.23x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                         |
| logging_silent                   | 40.6 ns                                                        | 34.0 ns: 1.19x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 40.3 ms: 1.19x faster                                                        |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 559 ms: 1.16x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 278 ms: 1.16x faster                                                         |
| pickle_pure_python               | 130 us                                                         | 114 us: 1.14x faster                                                         |
| html5lib                         | 23.1 ms                                                        | 20.2 ms: 1.14x faster                                                        |
| chaos                            | 24.3 ms                                                        | 21.3 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                         |
| xml_etree_process                | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.19 us: 1.10x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.1 ms: 1.08x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                         |
| mako                             | 4.41 ms                                                        | 4.12 ms: 1.07x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.1 ms: 1.07x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                         |
| connected_components             | 208 ms                                                         | 197 ms: 1.05x faster                                                         |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                        |
| thrift                           | 309 us                                                         | 294 us: 1.05x faster                                                         |
| raytrace                         | 109 ms                                                         | 104 ms: 1.04x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                        |
| genshi_text                      | 9.97 ms                                                        | 9.58 ms: 1.04x faster                                                        |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                         |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                        |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                        |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                        |
| sqlite_synth                     | 948 ns                                                         | 964 ns: 1.02x slower                                                         |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                        |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                        |
| django_template                  | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                         |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.50 ms: 1.13x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.15x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                        |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.20x slower                                                         |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                         |
| pylint                           | 106 ms                                                         | 141 ms: 1.34x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.3 ms: 2.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                 |

Benchmark hidden because not significant (2): docutils, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-2e5e9e6-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.136x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.20x