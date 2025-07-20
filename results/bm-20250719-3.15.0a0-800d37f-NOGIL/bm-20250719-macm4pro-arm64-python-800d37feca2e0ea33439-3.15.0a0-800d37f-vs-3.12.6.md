# Results vs. 3.12.6

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.098x faster
- HPT reliability: 97.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.4 ms: 2.02x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.0 ms: 1.01x slower                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 969 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.80 ms: 1.22x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 799 us: 2.51x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.88 ms: 2.10x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 85.4 ms: 2.02x faster                                                   |
| mdp                              | 1.09 sec                                                 | 574 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 495 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.93 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 816 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| go                               | 70.0 ms                                                  | 60.3 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.15x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.1 ns: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.8 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.02 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.04 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 969 ms: 1.01x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.0 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 328 us: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.3 us: 1.03x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 342 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 698 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 56.2 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.9 ms: 1.15x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.80 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 593 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): logging_simple
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-NOGIL/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 97.56% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x