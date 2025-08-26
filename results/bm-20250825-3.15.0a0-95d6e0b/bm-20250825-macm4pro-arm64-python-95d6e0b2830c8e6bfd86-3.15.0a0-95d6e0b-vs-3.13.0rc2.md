# Results vs. 3.13.0rc2

- fork: python
- ref: 95d6e0b2830c8e6bfd86
- machine: darwin-arm64
- commit hash: 95d6e0b
- commit date: 2025-08-25
- overall geometric mean: 1.031x faster
- HPT reliability: 97.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.9 ms: 2.97x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 927 ms: 1.08x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.79 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 951 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 54.9 ms: 1.32x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 927 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 922 us: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.7 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.2 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.79 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.0 ns: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.4 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.42 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.2 ms: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.48 us: 1.01x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 134 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.8 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 313 us: 1.56x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 16.9 ms: 2.70x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.9 ms: 2.97x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (5): sphinx, regex_compile, gc_traversal, genshi_xml, thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250825-3.15.0a0-95d6e0b/bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 97.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x