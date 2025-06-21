# Results vs. 3.12.6

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: darwin-arm64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.3 ms: 2.78x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.2 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.2 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.5 us: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 919 ms: 1.04x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.96 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.87 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.80 ms: 2.12x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.31 us: 1.35x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.7 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| float                            | 37.9 ms                                                  | 31.2 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.5 ms: 1.21x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 944 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.8 us: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.76 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.5 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.42 ms: 1.08x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.2 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.96 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.8 ms: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.5 us: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 919 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.8 ms: 1.02x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.76 us: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.87 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 714 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 939 us: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.3 ms: 2.78x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (4): logging_simple, json_loads, connected_components, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x