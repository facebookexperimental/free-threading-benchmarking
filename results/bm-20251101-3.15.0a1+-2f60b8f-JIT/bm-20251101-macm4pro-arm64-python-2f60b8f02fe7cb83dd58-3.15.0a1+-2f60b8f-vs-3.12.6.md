# Results vs. 3.12.6

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 228 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 94.2 us: 1.09x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| mdp                              | 1.09 sec                                                 | 556 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 228 ms: 1.95x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.40 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                    |
| go                               | 70.0 ms                                                  | 57.7 ms: 1.21x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                     |
| k_core                           | 1.12 sec                                                 | 933 ms: 1.20x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.18x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 17.9 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 288 ms: 1.14x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 584 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                   |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 94.2 us: 1.09x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 66.5 us: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.4 ms: 1.05x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.4 ms: 1.05x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.77 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.95 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 488 ms: 1.02x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.2 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.6 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 961 ns: 1.01x faster                                                     |
| thrift                           | 322 us                                                   | 320 us: 1.00x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sympy_str                        | 104 ms                                                   | 105 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.74 ms: 1.05x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.7 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 237 ms: 1.08x slower                                                     |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 367 us: 1.88x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): nbody, bench_thread_pool, sympy_sum
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-JIT/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.22x