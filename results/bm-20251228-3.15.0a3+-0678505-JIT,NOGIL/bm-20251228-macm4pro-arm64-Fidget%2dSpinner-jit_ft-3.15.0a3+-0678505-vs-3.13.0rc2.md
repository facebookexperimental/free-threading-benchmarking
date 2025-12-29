# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 0678505
- commit date: 2025-12-28
- overall geometric mean: 1.080x faster
- HPT reliability: 98.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                 |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                               |
| html5lib       | 23.1 ms                                                        | 22.1 ms: 1.04x faster                                                |
| sphinx         | 409 ms                                                         | 431 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                          | 1.01x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                 |
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                 |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                 |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                 |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                 |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                 |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                 |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                 |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                 |
| async_tree_eager                 | 43.2 ms                                                        | 43.9 ms: 1.02x slower                                                |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                |
| async_generators                 | 193 ms                                                         | 198 ms: 1.03x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                 |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.0 ms: 3.21x slower                                                |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                         |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                 |
| nbody          | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                          | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                |
| regex_compile  | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                |
| regex_dna      | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                          | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 78.3 us: 1.27x faster                                                |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                |
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                |
| tomli_loads          | 1000 ms                                                        | 849 ms: 1.18x faster                                                 |
| pickle_pure_python   | 130 us                                                         | 116 us: 1.12x faster                                                 |
| xml_etree_generate   | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                |
| xml_etree_process    | 25.4 ms                                                        | 23.8 ms: 1.06x faster                                                |
| xml_etree_parse      | 62.4 ms                                                        | 58.8 ms: 1.06x faster                                                |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                |
| Geometric mean       | (ref)                                                          | 1.13x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                |
| python_startup_no_site | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                                |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.74 ms: 1.08x slower                                                |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                |
| genshi_xml      | 21.4 ms                                                        | 28.3 ms: 1.32x slower                                                |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 812 us: 2.51x faster                                                 |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                 |
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                 |
| create_gc_cycles                 | 993 us                                                         | 514 us: 1.93x faster                                                 |
| richards                         | 22.1 ms                                                        | 11.5 ms: 1.92x faster                                                |
| richards_super                   | 24.7 ms                                                        | 13.8 ms: 1.79x faster                                                |
| async_tree_io_tg                 | 405 ms                                                         | 237 ms: 1.71x faster                                                 |
| subparsers                       | 6.26 ms                                                        | 3.88 ms: 1.62x faster                                                |
| mdp                              | 1.06 sec                                                       | 673 ms: 1.57x faster                                                 |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                 |
| k_core                           | 1.46 sec                                                       | 963 ms: 1.52x faster                                                 |
| pyflate                          | 222 ms                                                         | 148 ms: 1.50x faster                                                 |
| go                               | 72.6 ms                                                        | 49.0 ms: 1.48x faster                                                |
| scimark_sor                      | 64.0 ms                                                        | 44.3 ms: 1.45x faster                                                |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                |
| float                            | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                 |
| logging_silent                   | 40.6 ns                                                        | 31.4 ns: 1.29x faster                                                |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                 |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                 |
| unpickle_pure_python             | 99.5 us                                                        | 78.3 us: 1.27x faster                                                |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                 |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.7 ms: 1.26x faster                                                |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                 |
| deltablue                        | 1.45 ms                                                        | 1.20 ms: 1.21x faster                                                |
| tomli_loads                      | 1000 ms                                                        | 849 ms: 1.18x faster                                                 |
| fannkuch                         | 179 ms                                                         | 152 ms: 1.18x faster                                                 |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.81 sec: 1.18x faster                                               |
| scimark_monte_carlo              | 29.9 ms                                                        | 25.6 ms: 1.17x faster                                                |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                 |
| pprint_safe_repr                 | 322 ms                                                         | 283 ms: 1.14x faster                                                 |
| pickle_pure_python               | 130 us                                                         | 116 us: 1.12x faster                                                 |
| pprint_pformat                   | 650 ms                                                         | 581 ms: 1.12x faster                                                 |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.12x faster                                                 |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                 |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                 |
| xml_etree_generate               | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                |
| xml_etree_process                | 25.4 ms                                                        | 23.8 ms: 1.06x faster                                                |
| xml_etree_parse                  | 62.4 ms                                                        | 58.8 ms: 1.06x faster                                                |
| regex_compile                    | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                |
| pycparser                        | 470 ms                                                         | 449 ms: 1.05x faster                                                 |
| html5lib                         | 23.1 ms                                                        | 22.1 ms: 1.04x faster                                                |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                               |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                 |
| scimark_lu                       | 42.8 ms                                                        | 41.9 ms: 1.02x faster                                                |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                |
| spectral_norm                    | 43.7 ms                                                        | 43.9 ms: 1.00x slower                                                |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                 |
| async_tree_eager                 | 43.2 ms                                                        | 43.9 ms: 1.02x slower                                                |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                |
| regex_dna                        | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                |
| async_generators                 | 193 ms                                                         | 198 ms: 1.03x slower                                                 |
| thrift                           | 309 us                                                         | 319 us: 1.03x slower                                                 |
| crypto_pyaes                     | 33.6 ms                                                        | 34.8 ms: 1.04x slower                                                |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                |
| nbody                            | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                |
| sphinx                           | 409 ms                                                         | 431 ms: 1.05x slower                                                 |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                 |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                 |
| mako                             | 4.41 ms                                                        | 4.74 ms: 1.08x slower                                                |
| meteor_contest                   | 47.9 ms                                                        | 51.6 ms: 1.08x slower                                                |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.08x slower                                                |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                |
| typing_runtime_protocols         | 64.6 us                                                        | 70.1 us: 1.08x slower                                                |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                 |
| sympy_integrate                  | 7.53 ms                                                        | 8.49 ms: 1.13x slower                                                |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                |
| connected_components             | 208 ms                                                         | 239 ms: 1.15x slower                                                 |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                 |
| pylint                           | 106 ms                                                         | 128 ms: 1.22x slower                                                 |
| python_startup_no_site           | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                                |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                |
| sympy_sum                        | 52.3 ms                                                        | 64.1 ms: 1.23x slower                                                |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.23x slower                                                |
| sympy_str                        | 95.5 ms                                                        | 117 ms: 1.23x slower                                                 |
| sympy_expand                     | 159 ms                                                         | 196 ms: 1.23x slower                                                 |
| bench_mp_pool                    | 37.8 ms                                                        | 46.6 ms: 1.23x slower                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                 |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                |
| genshi_xml                       | 21.4 ms                                                        | 28.3 ms: 1.32x slower                                                |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                 |
| generators                       | 15.7 ms                                                        | 21.0 ms: 1.34x slower                                                |
| bench_thread_pool                | 412 us                                                         | 554 us: 1.35x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.0 ms: 3.21x slower                                                |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                         |

Benchmark hidden because not significant (3): json, hexiom, async_tree_eager_cpu_io_mixed
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251228-3.15.0a3+-0678505-JIT,NOGIL/bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 98.35% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x