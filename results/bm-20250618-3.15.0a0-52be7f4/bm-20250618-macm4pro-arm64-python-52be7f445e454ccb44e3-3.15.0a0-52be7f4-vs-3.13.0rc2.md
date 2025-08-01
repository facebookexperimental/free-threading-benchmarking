# Results vs. 3.13.0rc2

- fork: python
- ref: 52be7f445e454ccb44e3
- machine: darwin-arm64
- commit hash: 52be7f4
- commit date: 2025-06-18
- overall geometric mean: 1.022x faster
- HPT reliability: 69.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 946 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| go                               | 72.6 ms                                                        | 57.0 ms: 1.27x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.74 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 967 us: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.48 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 955 ns: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.0 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.4 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.29 us: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 721 ms: 1.11x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.3 ms: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.7 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.84 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (6): json_loads, pathlib, richards, genshi_text, sphinx, richards_super
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 69.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x