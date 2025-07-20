# Results vs. 3.12.6

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.086x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.03x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.0 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.45 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                   |
| mako            | 4.77 ms                                                  | 5.01 ms: 1.05x slower                                                   |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 524 ms: 2.08x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.99 ms: 2.08x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.39x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.50 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| float                            | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.2 ns: 1.21x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.2 ms: 1.19x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.7 ms: 1.19x faster                                                   |
| go                               | 70.0 ms                                                  | 58.8 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| k_core                           | 1.12 sec                                                 | 962 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.3 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.1 us: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.63 ms: 1.05x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.0 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.0 ms: 1.02x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.4 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 506 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 340 ms: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.04x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.45 ms: 1.04x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.01 ms: 1.05x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.07x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 978 us: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.5 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (5): json, scimark_lu, sympy_sum, regex_dna, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x