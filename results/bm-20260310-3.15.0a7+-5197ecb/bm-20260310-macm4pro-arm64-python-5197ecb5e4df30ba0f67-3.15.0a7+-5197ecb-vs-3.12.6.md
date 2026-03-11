# Results vs. 3.12.6

- fork: python
- ref: 5197ecb5e4df30ba0f67
- machine: darwin-arm64
- commit hash: 5197ecb
- commit date: 2026-03-10
- overall geometric mean: 1.134x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.5 ms: 2.63x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.4 ms: 1.25x faster                                                    |
| tomli_loads          | 957 ms                                                   | 853 ms: 1.12x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.00x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                     |
| mdp                              | 1.09 sec                                                 | 554 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.53x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.58 us: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| go                               | 70.0 ms                                                  | 56.0 ms: 1.25x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.4 ms: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| k_core                           | 1.12 sec                                                 | 909 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| raytrace                         | 145 ms                                                   | 120 ms: 1.20x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 51.2 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.18x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.4 ns: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.0 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 853 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.1 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.7 us: 1.08x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.88 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.66 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 640 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 317 ms: 1.03x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 57.2 ms: 1.01x faster                                                    |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 39.2 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                     |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.04x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 176 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.4 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 911 us: 1.10x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 257 us: 1.32x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.5 ms: 2.63x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (2): json_loads, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260310-3.15.0a7+-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.134x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.24x