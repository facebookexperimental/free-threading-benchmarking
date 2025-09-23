# Results vs. 3.13.0rc2

- fork: python
- ref: 49e83e31bd45e513a3ca
- machine: darwin-arm64
- commit hash: 49e83e3
- commit date: 2025-09-22
- overall geometric mean: 1.044x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.0 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 892 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.0 us: 1.02x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.84 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 245 ms: 2.12x faster                                                    |
| mdp                              | 1.06 sec                                                       | 524 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                   |
| go                               | 72.6 ms                                                        | 55.6 ms: 1.30x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 892 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 901 us: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.87 ms: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.7 ms: 1.08x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.3 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.05x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.00 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.0 us: 1.02x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.1 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.84 ms: 1.01x faster                                                   |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 937 ns: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.3 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 54.7 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 40.9 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.4 ms: 1.08x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.44 us: 1.09x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 312 us: 1.56x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.3 ms: 2.76x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.0 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (3): thrift, python_startup, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250922-3.15.0a0-49e83e3/bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x