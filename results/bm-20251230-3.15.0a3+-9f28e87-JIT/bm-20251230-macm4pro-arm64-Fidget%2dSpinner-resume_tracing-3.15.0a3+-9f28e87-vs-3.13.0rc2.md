# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 9f28e87
- commit date: 2025-12-30
- overall geometric mean: 1.122x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                         |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                       |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 216 ms: 1.87x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.68x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 98.8 ms: 1.44x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.40x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 94.9 ms: 1.40x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                        |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.1 ms: 2.80x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.9 ms: 1.07x faster                                                        |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                        |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 73.2 us: 1.36x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                        |
| tomli_loads          | 1000 ms                                                        | 801 ms: 1.25x faster                                                         |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.20x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 114 us: 1.14x faster                                                         |
| xml_etree_process    | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 32.0 ms: 1.12x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.93 ms: 1.03x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.19 ms: 1.05x faster                                                        |
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                        |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                        |
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                        |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                         |
| richards                         | 22.1 ms                                                        | 11.4 ms: 1.93x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 13.2 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 216 ms: 1.87x faster                                                         |
| k_core                           | 1.46 sec                                                       | 867 ms: 1.69x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.68x faster                                                         |
| scimark_sor                      | 64.0 ms                                                        | 38.1 ms: 1.68x faster                                                        |
| mdp                              | 1.06 sec                                                       | 645 ms: 1.64x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.94 ms: 1.59x faster                                                        |
| go                               | 72.6 ms                                                        | 46.0 ms: 1.58x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 98.8 ms: 1.44x faster                                                        |
| pyflate                          | 222 ms                                                         | 154 ms: 1.44x faster                                                         |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.40x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 94.9 ms: 1.40x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 73.2 us: 1.36x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.0 ms: 1.30x faster                                                        |
| float                            | 31.4 ms                                                        | 24.4 ms: 1.29x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 801 ms: 1.25x faster                                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.20 ms: 1.21x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 102 ms: 1.21x faster                                                         |
| logging_silent                   | 40.6 ns                                                        | 33.8 ns: 1.20x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.20x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.87 us: 1.20x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                         |
| logging_format                   | 2.45 us                                                        | 2.05 us: 1.19x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 280 ms: 1.15x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 568 ms: 1.14x faster                                                         |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                         |
| pickle_pure_python               | 130 us                                                         | 114 us: 1.14x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 22.4 ms: 1.13x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 32.0 ms: 1.12x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| chaos                            | 24.3 ms                                                        | 22.1 ms: 1.10x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.3 ms: 1.08x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.9 ms: 1.07x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.2 ms: 1.06x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 937 us: 1.06x faster                                                         |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 45.4 ms: 1.05x faster                                                        |
| connected_components             | 208 ms                                                         | 197 ms: 1.05x faster                                                         |
| mako                             | 4.41 ms                                                        | 4.19 ms: 1.05x faster                                                        |
| thrift                           | 309 us                                                         | 295 us: 1.05x faster                                                         |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                        |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| scimark_lu                       | 42.8 ms                                                        | 41.5 ms: 1.03x faster                                                        |
| raytrace                         | 109 ms                                                         | 106 ms: 1.03x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                         |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                        |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                        |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                         |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.00x faster                                                        |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                         |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                        |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                         |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.93 ms: 1.03x slower                                                        |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                         |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                        |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                        |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.95 ms: 1.10x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.34 ms: 1.11x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 7.70 us: 1.13x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                         |
| pylint                           | 106 ms                                                         | 125 ms: 1.19x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 63.5 ms: 1.21x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 122 ms: 1.28x slower                                                         |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                         |
| generators                       | 15.7 ms                                                        | 21.4 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.1 ms: 2.80x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                 |

Benchmark hidden because not significant (2): sphinx, xml_etree_parse
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (2) of results/bm-20251230-3.15.0a3+-9f28e87-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87.json: sqlglot_v2_normalize, sqlglot_v2_optimize

- Geometric mean (including insignificant results): 1.122x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x