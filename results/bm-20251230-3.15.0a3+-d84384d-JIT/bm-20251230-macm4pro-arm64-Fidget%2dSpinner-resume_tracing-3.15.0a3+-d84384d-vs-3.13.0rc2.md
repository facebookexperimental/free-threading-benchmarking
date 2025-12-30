# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d84384d
- commit date: 2025-12-30
- overall geometric mean: 1.131x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                         |
| html5lib       | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                        |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.44x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.44x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 211 ms: 1.92x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 96.8 ms: 1.47x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 93.7 ms: 1.42x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                         |
| coroutines                       | 10.8 ms                                                        | 9.57 ms: 1.12x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                        |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.7 ms: 1.07x faster                                                        |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                        |
| regex_compile  | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.7 us: 1.37x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 806 ms: 1.24x faster                                                         |
| pickle_pure_python   | 130 us                                                         | 111 us: 1.17x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 33.3 ms: 1.07x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.06 ms: 1.05x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.51 ms: 1.09x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.36 ms: 1.07x faster                                                        |
| mako            | 4.41 ms                                                        | 4.16 ms: 1.06x faster                                                        |
| django_template | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.44x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.44x faster                                                         |
| richards                         | 22.1 ms                                                        | 10.1 ms: 2.18x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.9 ms: 2.07x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 211 ms: 1.92x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                         |
| k_core                           | 1.46 sec                                                       | 869 ms: 1.68x faster                                                         |
| mdp                              | 1.06 sec                                                       | 642 ms: 1.65x faster                                                         |
| scimark_sor                      | 64.0 ms                                                        | 40.0 ms: 1.60x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.93 ms: 1.59x faster                                                        |
| go                               | 72.6 ms                                                        | 48.9 ms: 1.48x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 96.8 ms: 1.47x faster                                                        |
| pyflate                          | 222 ms                                                         | 152 ms: 1.46x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                        |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 93.7 ms: 1.42x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 72.7 us: 1.37x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.07 ms: 1.35x faster                                                        |
| float                            | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.28x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.8 ms: 1.25x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 806 ms: 1.24x faster                                                         |
| logging_format                   | 2.45 us                                                        | 1.98 us: 1.23x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.82 us: 1.23x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 265 ms: 1.21x faster                                                         |
| scimark_fft                      | 124 ms                                                         | 103 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 543 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                         |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 34.1 ns: 1.19x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 111 us: 1.17x faster                                                         |
| scimark_lu                       | 42.8 ms                                                        | 36.8 ms: 1.16x faster                                                        |
| fannkuch                         | 179 ms                                                         | 154 ms: 1.16x faster                                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                         |
| chaos                            | 24.3 ms                                                        | 21.6 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.57 ms: 1.12x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.6 ms: 1.12x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.79 ms: 1.09x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.3 ms: 1.08x faster                                                        |
| thrift                           | 309 us                                                         | 287 us: 1.08x faster                                                         |
| xml_etree_generate               | 35.8 ms                                                        | 33.3 ms: 1.07x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.7 ms: 1.07x faster                                                        |
| genshi_text                      | 9.97 ms                                                        | 9.36 ms: 1.07x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.2 ms: 1.06x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.16 ms: 1.06x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 942 us: 1.06x faster                                                         |
| raytrace                         | 109 ms                                                         | 103 ms: 1.05x faster                                                         |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                        |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                        |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                         |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 46.5 ms: 1.03x faster                                                        |
| regex_compile                    | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                        |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                        |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                        |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                         |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                        |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                        |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                        |
| sqlite_synth                     | 948 ns                                                         | 974 ns: 1.03x slower                                                         |
| django_template                  | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 9.06 ms: 1.05x slower                                                        |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                         |
| hexiom                           | 2.85 ms                                                        | 3.01 ms: 1.06x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.51 ms: 1.09x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 7.72 us: 1.13x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.58 ms: 1.14x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.15x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 65.6 ms: 1.25x slower                                                        |
| generators                       | 15.7 ms                                                        | 19.9 ms: 1.27x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 122 ms: 1.27x slower                                                         |
| many_optionals                   | 200 us                                                         | 258 us: 1.28x slower                                                         |
| pylint                           | 106 ms                                                         | 140 ms: 1.32x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                 |

Benchmark hidden because not significant (2): docutils, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251230-3.15.0a3+-d84384d-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d84384d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.131x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.20x