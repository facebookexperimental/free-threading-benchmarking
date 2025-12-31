# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 564677c
- commit date: 2025-12-31
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                         |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                       |
| html5lib       | 23.1 ms                                                        | 19.5 ms: 1.19x faster                                                        |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 211 ms: 2.49x faster                                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 210 ms: 2.48x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 94.5 ms: 1.51x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 92.7 ms: 1.43x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.39x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.22x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 38.2 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.3 ms: 2.67x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.2 ms: 1.30x faster                                                        |
| nbody          | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                        |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.8 ms: 1.20x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.6 us: 1.37x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 784 ms: 1.28x faster                                                         |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.0 ms: 1.25x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 112 us: 1.16x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.3 ms: 1.14x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                        |
| Geometric mean       | (ref)                                                          | 1.18x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.14 ms: 1.09x faster                                                        |
| mako            | 4.41 ms                                                        | 4.11 ms: 1.07x faster                                                        |
| django_template | 12.5 ms                                                        | 13.0 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 211 ms: 2.49x faster                                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 210 ms: 2.48x faster                                                         |
| richards                         | 22.1 ms                                                        | 9.43 ms: 2.34x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.4 ms: 2.17x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                         |
| k_core                           | 1.46 sec                                                       | 864 ms: 1.69x faster                                                         |
| go                               | 72.6 ms                                                        | 44.2 ms: 1.64x faster                                                        |
| mdp                              | 1.06 sec                                                       | 648 ms: 1.63x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.86 ms: 1.62x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 40.5 ms: 1.58x faster                                                        |
| pyflate                          | 222 ms                                                         | 144 ms: 1.54x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 94.5 ms: 1.51x faster                                                        |
| deepcopy                         | 145 us                                                         | 98.4 us: 1.47x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 92.7 ms: 1.43x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.39x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 72.6 us: 1.37x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.08 ms: 1.35x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.3 ms: 1.34x faster                                                        |
| float                            | 31.4 ms                                                        | 24.2 ms: 1.30x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.29x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.64 ms: 1.28x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 784 ms: 1.28x faster                                                         |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.0 ms: 1.25x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 529 ms: 1.23x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 263 ms: 1.22x faster                                                         |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.22x faster                                                         |
| logging_silent                   | 40.6 ns                                                        | 33.6 ns: 1.21x faster                                                        |
| regex_compile                    | 47.9 ms                                                        | 39.8 ms: 1.20x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 19.5 ms: 1.19x faster                                                        |
| fannkuch                         | 179 ms                                                         | 152 ms: 1.17x faster                                                         |
| chaos                            | 24.3 ms                                                        | 20.8 ms: 1.17x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 112 us: 1.16x faster                                                         |
| scimark_lu                       | 42.8 ms                                                        | 37.0 ms: 1.16x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.86 sec: 1.14x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 22.3 ms: 1.14x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 38.2 ms: 1.13x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 2.01 us: 1.11x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.23 us: 1.10x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.21 us: 1.10x faster                                                        |
| genshi_text                      | 9.97 ms                                                        | 9.14 ms: 1.09x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 912 us: 1.09x faster                                                         |
| crypto_pyaes                     | 33.6 ms                                                        | 30.9 ms: 1.09x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 40.6 ms: 1.08x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.11 ms: 1.07x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                        |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                        |
| raytrace                         | 109 ms                                                         | 102 ms: 1.06x faster                                                         |
| nbody                            | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                        |
| thrift                           | 309 us                                                         | 291 us: 1.06x faster                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                        |
| connected_components             | 208 ms                                                         | 197 ms: 1.06x faster                                                         |
| hexiom                           | 2.85 ms                                                        | 2.72 ms: 1.05x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                         |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                         |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.8 us: 1.03x faster                                                        |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                       |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                         |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                         |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                        |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                        |
| django_template                  | 12.5 ms                                                        | 13.0 ms: 1.04x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                         |
| nqueens                          | 37.2 ms                                                        | 39.4 ms: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.22 ms: 1.09x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.13x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                        |
| pylint                           | 106 ms                                                         | 125 ms: 1.18x slower                                                         |
| sympy_str                        | 95.5 ms                                                        | 114 ms: 1.19x slower                                                         |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                         |
| generators                       | 15.7 ms                                                        | 19.7 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.3 ms: 2.67x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                                 |

Benchmark hidden because not significant (2): genshi_xml, regex_dna
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-564677c-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x