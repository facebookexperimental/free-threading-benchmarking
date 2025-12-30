# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d52a106
- commit date: 2025-12-30
- overall geometric mean: 1.169x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.03x faster                                                         |
| html5lib       | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                        |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 210 ms: 2.48x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 214 ms: 2.45x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 211 ms: 1.92x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 94.4 ms: 1.51x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 92.4 ms: 1.44x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 38.5 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.9 ms: 1.06x faster                                                        |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                          | 1.12x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                        |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.5 us: 1.37x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 786 ms: 1.27x faster                                                         |
| json_dumps           | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 111 us: 1.17x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 33.3 ms: 1.07x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.29 ms: 1.07x faster                                                        |
| mako            | 4.41 ms                                                        | 4.17 ms: 1.06x faster                                                        |
| django_template | 12.5 ms                                                        | 12.9 ms: 1.03x slower                                                        |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 210 ms: 2.48x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 214 ms: 2.45x faster                                                         |
| richards                         | 22.1 ms                                                        | 9.51 ms: 2.32x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.5 ms: 2.16x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 211 ms: 1.92x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                         |
| k_core                           | 1.46 sec                                                       | 864 ms: 1.69x faster                                                         |
| mdp                              | 1.06 sec                                                       | 641 ms: 1.65x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.85 ms: 1.63x faster                                                        |
| go                               | 72.6 ms                                                        | 44.9 ms: 1.62x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 40.5 ms: 1.58x faster                                                        |
| pyflate                          | 222 ms                                                         | 147 ms: 1.51x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 94.4 ms: 1.51x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 92.4 ms: 1.44x faster                                                        |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 72.5 us: 1.37x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.06 ms: 1.36x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.6 ms: 1.32x faster                                                        |
| float                            | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 786 ms: 1.27x faster                                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                         |
| logging_format                   | 2.45 us                                                        | 2.00 us: 1.22x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.83 us: 1.22x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.22x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 532 ms: 1.22x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 265 ms: 1.22x faster                                                         |
| telco                            | 3.07 ms                                                        | 2.58 ms: 1.19x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 34.3 ns: 1.18x faster                                                        |
| fannkuch                         | 179 ms                                                         | 151 ms: 1.18x faster                                                         |
| scimark_lu                       | 42.8 ms                                                        | 36.5 ms: 1.17x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 111 us: 1.17x faster                                                         |
| xml_etree_process                | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                       |
| chaos                            | 24.3 ms                                                        | 21.4 ms: 1.14x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 38.5 ms: 1.12x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 915 us: 1.09x faster                                                         |
| crypto_pyaes                     | 33.6 ms                                                        | 31.3 ms: 1.08x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 33.3 ms: 1.07x faster                                                        |
| thrift                           | 309 us                                                         | 288 us: 1.07x faster                                                         |
| genshi_text                      | 9.97 ms                                                        | 9.29 ms: 1.07x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 45.0 ms: 1.07x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.9 ms: 1.06x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.17 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.4 ms: 1.06x faster                                                        |
| raytrace                         | 109 ms                                                         | 104 ms: 1.05x faster                                                         |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                         |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                         |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                        |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                        |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                        |
| 2to3                             | 112 ms                                                         | 109 ms: 1.03x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                        |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.00x slower                                                        |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                        |
| sqlite_synth                     | 948 ns                                                         | 965 ns: 1.02x slower                                                         |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                        |
| django_template                  | 12.5 ms                                                        | 12.9 ms: 1.03x slower                                                        |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                         |
| nqueens                          | 37.2 ms                                                        | 39.4 ms: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 7.69 us: 1.13x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                        |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                         |
| generators                       | 15.7 ms                                                        | 19.8 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                                 |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (17) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, docutils, gevent_hub, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
Ignored benchmarks (2) of results/bm-20251230-3.15.0a3+-d52a106-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106.json: sqlglot_v2_optimize, sqlglot_v2_parse

- Geometric mean (including insignificant results): 1.169x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x