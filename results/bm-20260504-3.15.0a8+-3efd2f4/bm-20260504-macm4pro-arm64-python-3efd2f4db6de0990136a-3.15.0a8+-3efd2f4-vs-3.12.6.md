# Results vs. 3.12.6

- fork: python
- ref: 3efd2f4db6de0990136a
- machine: darwin-arm64
- commit hash: 3efd2f4
- commit date: 2026-05-04
- overall geometric mean: 1.137x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 964 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 307 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.50x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 309 ms: 1.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.17x slower                                                     |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                    |
| tomli_loads          | 957 ms                                                   | 836 ms: 1.15x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.7 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 68.5 ms: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.70 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.97 ms: 5.23x faster                                                    |
| pylint                           | 128 ms                                                   | 56.8 ms: 2.26x faster                                                    |
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 307 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.50x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 309 ms: 1.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.94 us: 1.42x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                    |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.1 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.3 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                     |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 836 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.3 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.6 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                    |
| fannkuch                         | 176 ms                                                   | 164 ms: 1.07x faster                                                     |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 624 ms: 1.07x faster                                                     |
| docutils                         | 1.02 sec                                                 | 964 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.7 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.7 us: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                     |
| thrift                           | 322 us                                                   | 314 us: 1.02x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.97 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 68.5 ms: 1.01x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.2 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.1 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 877 us: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.4 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.9 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.17x slower                                                     |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260504-3.15.0a8+-3efd2f4/bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.137x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x