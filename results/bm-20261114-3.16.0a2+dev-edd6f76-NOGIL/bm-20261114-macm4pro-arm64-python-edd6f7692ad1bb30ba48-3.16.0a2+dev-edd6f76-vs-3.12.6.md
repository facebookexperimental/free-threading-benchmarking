# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.074x faster
- HPT reliability: 92.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| sphinx         | 434 ms                                                   | 446 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 111 ms: 1.87x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 300 ms: 1.65x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 299 ms: 1.60x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 300 ms: 1.53x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 296 ms: 1.51x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 141 ms: 1.27x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.55x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| pidigits       | 161 ms                                                   | 147 ms: 1.10x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.2 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.8 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                       |
| tomli_loads          | 957 ms                                                   | 869 ms: 1.10x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.0 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 158 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.21x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.29 ms: 4.84x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                        |
| pylint                           | 128 ms                                                   | 51.8 ms: 2.47x faster                                                       |
| mdp                              | 1.09 sec                                                 | 566 ms: 1.93x faster                                                        |
| async_generators                 | 206 ms                                                   | 111 ms: 1.87x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 472 us: 1.76x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 300 ms: 1.65x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 299 ms: 1.60x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 300 ms: 1.53x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 296 ms: 1.51x faster                                                        |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.2 us: 1.33x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.4 us: 1.27x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 141 ms: 1.27x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.17x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                        |
| go                               | 70.0 ms                                                  | 60.2 ms: 1.16x faster                                                       |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.13x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 869 ms: 1.10x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.5 ms: 1.10x faster                                                       |
| pidigits                         | 161 ms                                                   | 147 ms: 1.10x faster                                                        |
| pyflate                          | 216 ms                                                   | 197 ms: 1.09x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                       |
| raytrace                         | 145 ms                                                   | 136 ms: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 58.5 ms: 1.04x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.3 ns: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| pycparser                        | 497 ms                                                   | 490 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                       |
| sphinx                           | 434 ms                                                   | 446 ms: 1.03x slower                                                        |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.1 ms: 1.03x slower                                                       |
| deltablue                        | 1.73 ms                                                  | 1.79 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                       |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.06x slower                                                        |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                        |
| generators                       | 21.9 ms                                                  | 23.5 ms: 1.07x slower                                                       |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.6 ms: 1.07x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.0 ms: 1.09x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                       |
| nbody                            | 54.2 ms                                                  | 59.2 ms: 1.09x slower                                                       |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 52.6 ms: 1.10x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                       |
| shortest_path                    | 219 ms                                                   | 244 ms: 1.12x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 468 us: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 158 us: 1.13x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 63.8 ms: 1.17x slower                                                       |
| connected_components             | 201 ms                                                   | 237 ms: 1.18x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 65.7 ms: 1.28x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.3 ms: 1.54x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.55x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (2): chaos, json
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-NOGIL/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 92.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x