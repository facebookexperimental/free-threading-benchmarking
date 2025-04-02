# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: darwin-arm64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.105x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 833 ms: 1.15x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 46.9 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.96 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.56 ms: 2.43x faster                                                    |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.54 us: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                    |
| go                               | 70.0 ms                                                  | 56.1 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.2 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| k_core                           | 1.12 sec                                                 | 959 ms: 1.17x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 833 ms: 1.15x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.7 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.55 us: 1.10x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.9 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.4 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.07x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.2 us: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 37.4 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.0 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.5 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.7 ms: 1.05x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.69 ms: 1.04x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 137 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 486 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.01x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 39.4 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 52.4 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 895 us: 1.08x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.96 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 229 us: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.12 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): json, pprint_pformat, sqlalchemy_imperative
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.12x