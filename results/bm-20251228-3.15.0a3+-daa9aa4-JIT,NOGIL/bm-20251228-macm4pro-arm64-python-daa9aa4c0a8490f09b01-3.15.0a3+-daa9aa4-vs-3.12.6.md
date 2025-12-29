# Results vs. 3.12.6

- fork: python
- ref: daa9aa4c0a8490f09b01
- machine: darwin-arm64
- commit hash: daa9aa4
- commit date: 2025-12-28
- overall geometric mean: 1.072x faster
- HPT reliability: 91.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.09x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 256 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.2 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.07 ms: 1.05x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.02 sec: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.22 ms: 4.92x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 819 us: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 256 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                     |
| mdp                              | 1.09 sec                                                 | 635 ms: 1.72x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 512 us: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.60 us: 1.14x faster                                                    |
| go                               | 70.0 ms                                                  | 61.2 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.0 ns: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.07 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.3 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.68 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.9 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 338 ms: 1.03x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.35 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 45.9 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.22 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.02 sec: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.2 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                     |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.09x slower                                                     |
| 2to3                             | 114 ms                                                   | 125 ms: 1.09x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 63.2 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.9 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| shortest_path                    | 219 ms                                                   | 257 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.1 ms: 1.20x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 249 ms: 1.24x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 278 us: 1.43x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.2 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (4): fannkuch, sphinx, asyncio_websockets, typing_runtime_protocols
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251228-3.15.0a3+-daa9aa4-JIT,NOGIL/bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 91.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x