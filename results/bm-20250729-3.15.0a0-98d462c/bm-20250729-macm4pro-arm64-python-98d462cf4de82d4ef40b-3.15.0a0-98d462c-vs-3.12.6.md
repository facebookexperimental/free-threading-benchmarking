# Results vs. 3.12.6

- fork: python
- ref: 98d462cf4de82d4ef40b
- machine: darwin-arm64
- commit hash: 98d462c
- commit date: 2025-07-29
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.8 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.5 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.7 us: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 936 ms: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.51 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.56 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.5 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.24x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 30.8 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 958 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.5 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.2 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.4 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.7 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.0 ms: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 936 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 653 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 324 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 959 ns: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.51 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 948 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 326 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (5): pycparser, json, genshi_xml, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250729-3.15.0a0-98d462c/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x