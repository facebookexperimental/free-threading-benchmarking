# Results vs. 3.13.0rc2

- fork: python
- ref: 81c975bcfc1ac0533f94
- machine: darwin-arm64
- commit hash: 81c975b
- commit date: 2025-09-17
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.57x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.9 ms: 1.11x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 11.2 ms: 1.05x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.09x slower                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.77 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 795 ms: 1.26x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.2 us: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.03 ms: 1.10x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.21x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                    |
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 952 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.2 us: 1.49x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                   |
| go                               | 72.6 ms                                                        | 50.5 ms: 1.44x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.6 ms: 1.27x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 795 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.1 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.75 ms: 1.12x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 38.9 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| genshi_text                      | 9.97 ms                                                        | 9.03 ms: 1.10x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.10x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.5 ms: 1.10x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 918 us: 1.08x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 92.2 us: 1.08x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.7 us: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| thrift                           | 309 us                                                         | 292 us: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.17 ms: 1.05x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.05x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 38.9 ns: 1.04x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 626 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 93.8 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.02x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.00x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 52.7 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.97 us: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| pylint                           | 106 ms                                                         | 109 ms: 1.03x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.59 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.0 ms: 1.05x slower                                                   |
| regex_v8                         | 10.7 ms                                                        | 11.2 ms: 1.05x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 45.1 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.06x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.09x slower                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.77 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 313 us: 1.56x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.3 ms: 2.77x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): bench_thread_pool
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250917-3.15.0a0-81c975b-CLANG/bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.09x