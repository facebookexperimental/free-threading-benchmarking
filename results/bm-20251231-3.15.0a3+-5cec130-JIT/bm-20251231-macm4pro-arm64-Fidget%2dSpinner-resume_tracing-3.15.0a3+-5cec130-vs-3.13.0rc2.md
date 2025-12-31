# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.152x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                       |
| html5lib       | 23.1 ms                                                        | 19.7 ms: 1.18x faster                                                        |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                 |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 212 ms: 2.46x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 223 ms: 1.73x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 96.1 ms: 1.48x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 92.7 ms: 1.43x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.2 ms: 1.30x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.4 ms: 1.08x faster                                                        |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.7 ms: 1.21x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.4 us: 1.37x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 793 ms: 1.26x faster                                                         |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 110 us: 1.18x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.0 ms: 1.15x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 33.0 ms: 1.09x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.10 ms: 1.08x faster                                                        |
| genshi_text     | 9.97 ms                                                        | 9.37 ms: 1.06x faster                                                        |
| django_template | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 212 ms: 2.46x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                         |
| richards                         | 22.1 ms                                                        | 10.2 ms: 2.17x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.9 ms: 2.08x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 223 ms: 1.73x faster                                                         |
| go                               | 72.6 ms                                                        | 42.0 ms: 1.73x faster                                                        |
| k_core                           | 1.46 sec                                                       | 863 ms: 1.70x faster                                                         |
| mdp                              | 1.06 sec                                                       | 634 ms: 1.67x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 40.4 ms: 1.58x faster                                                        |
| pyflate                          | 222 ms                                                         | 143 ms: 1.55x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 96.1 ms: 1.48x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 92.7 ms: 1.43x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| deepcopy                         | 145 us                                                         | 102 us: 1.42x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 72.4 us: 1.37x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.09 ms: 1.33x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.5 ms: 1.33x faster                                                        |
| float                            | 31.4 ms                                                        | 24.2 ms: 1.30x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 793 ms: 1.26x faster                                                         |
| logging_simple                   | 2.24 us                                                        | 1.79 us: 1.25x faster                                                        |
| logging_format                   | 2.45 us                                                        | 1.97 us: 1.24x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.23x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 531 ms: 1.22x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 263 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 39.7 ms: 1.21x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                         |
| telco                            | 3.07 ms                                                        | 2.58 ms: 1.19x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 34.2 ns: 1.19x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 110 us: 1.18x faster                                                         |
| html5lib                         | 23.1 ms                                                        | 19.7 ms: 1.18x faster                                                        |
| scimark_lu                       | 42.8 ms                                                        | 36.5 ms: 1.17x faster                                                        |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                         |
| chaos                            | 24.3 ms                                                        | 21.0 ms: 1.16x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 22.0 ms: 1.15x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                         |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.22 us: 1.09x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 914 us: 1.09x faster                                                         |
| xml_etree_generate               | 35.8 ms                                                        | 33.0 ms: 1.09x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.0 ms: 1.08x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.4 ms: 1.08x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.10 ms: 1.08x faster                                                        |
| thrift                           | 309 us                                                         | 287 us: 1.08x faster                                                         |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                        |
| raytrace                         | 109 ms                                                         | 102 ms: 1.07x faster                                                         |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                        |
| genshi_text                      | 9.97 ms                                                        | 9.37 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.2 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| connected_components             | 208 ms                                                         | 197 ms: 1.05x faster                                                         |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                        |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                         |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                         |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                         |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                         |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                        |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                        |
| django_template                  | 12.5 ms                                                        | 13.1 ms: 1.05x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                         |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.06x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.33 ms: 1.11x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.12x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.20x slower                                                         |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.21x slower                                                        |
| pylint                           | 106 ms                                                         | 133 ms: 1.26x slower                                                         |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                                 |

Benchmark hidden because not significant (4): 2to3, regex_dna, gc_traversal, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-5cec130-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.152x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x