# Results vs. 3.12.6

- fork: python
- ref: 7a4c6dfb8839eb05fb87
- machine: darwin-arm64
- commit hash: 7a4c6df
- commit date: 2026-05-11
- overall geometric mean: 1.115x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 435 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 278 ms: 1.79x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 270 ms: 1.78x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 274 ms: 1.63x faster                                                    |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 131 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 279 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 285 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.11x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 179 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 262 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 109 ms: 3.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.3 ms: 1.17x faster                                                   |
| pidigits       | 161 ms                                                   | 156 ms: 1.03x faster                                                    |
| nbody          | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.0 ms: 1.09x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 8.99 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 839 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.2 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                    |
| pylint                           | 128 ms                                                   | 52.6 ms: 2.44x faster                                                   |
| mdp                              | 1.09 sec                                                 | 584 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 278 ms: 1.79x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 270 ms: 1.78x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 506 us: 1.64x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 274 ms: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 104 us: 1.56x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 131 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 54.6 us: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.28x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 785 ns: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.04 us: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 279 ms: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 57.9 ms: 1.21x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.4 ns: 1.20x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                  |
| float                            | 37.9 ms                                                  | 32.3 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 285 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 839 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.30 us: 1.12x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.11x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.0 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.56 us: 1.09x faster                                                   |
| pycparser                        | 497 ms                                                   | 456 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 50.2 ms: 1.08x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.5 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.5 ms: 1.07x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 8.99 ms: 1.07x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 179 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                    |
| pidigits                         | 161 ms                                                   | 156 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.9 ms: 1.01x faster                                                   |
| sphinx                           | 434 ms                                                   | 435 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 678 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.1 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.2 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.1 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.9 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 60.6 ms: 1.18x slower                                                   |
| connected_components             | 201 ms                                                   | 242 ms: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 262 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.3 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 109 ms: 3.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): dask, async_tree_eager
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.34x