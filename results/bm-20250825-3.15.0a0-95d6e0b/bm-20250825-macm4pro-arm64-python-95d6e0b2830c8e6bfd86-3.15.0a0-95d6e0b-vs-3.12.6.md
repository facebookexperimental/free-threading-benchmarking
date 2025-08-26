# Results vs. 3.12.6

- fork: python
- ref: 95d6e0b2830c8e6bfd86
- machine: darwin-arm64
- commit hash: 95d6e0b
- commit date: 2025-08-25
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.9 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 927 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.79 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| go                               | 70.0 ms                                                  | 54.9 ms: 1.28x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.0 ns: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.24x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.2 ms: 1.23x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 16.9 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 951 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.5 us: 1.14x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.4 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.42 ms: 1.08x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.79 ms: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.7 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 936 ns: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 927 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 490 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 662 ms: 1.00x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 922 us: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 313 us: 1.60x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.9 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): connected_components, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250825-3.15.0a0-95d6e0b/bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x