# Results vs. 3.12.6

- fork: python
- ref: e66f87ca73516efb4aec
- machine: darwin-arm64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| tomli_loads          | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 229 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.51 us: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.0 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| go                               | 70.0 ms                                                  | 56.2 ms: 1.25x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 901 ms: 1.24x faster                                                     |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.5 ns: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.55 us: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.8 ms: 1.07x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.5 us: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.0 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.8 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 317 us: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 660 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.7 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 898 us: 1.08x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 367 us: 1.88x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): html5lib, bench_thread_pool, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.20x