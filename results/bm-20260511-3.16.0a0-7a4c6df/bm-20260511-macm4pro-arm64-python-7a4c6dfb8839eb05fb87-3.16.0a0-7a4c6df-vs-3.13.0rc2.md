# Results vs. 3.13.0rc2

- fork: python
- ref: 7a4c6dfb8839eb05fb87
- machine: darwin-arm64
- commit hash: 7a4c6df
- commit date: 2026-05-11
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 947 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                   |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 300 ms: 1.75x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 326 ms: 1.60x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 305 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 324 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 123 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 276 ms: 1.07x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 100 ms: 3.47x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| nbody          | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 814 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 501 ms: 2.11x faster                                                    |
| pylint                           | 106 ms                                                         | 55.4 ms: 1.91x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 300 ms: 1.75x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 326 ms: 1.60x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 98.0 us: 1.48x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.46x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                   |
| go                               | 72.6 ms                                                        | 51.9 ms: 1.40x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 48.0 us: 1.35x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.34x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 305 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 324 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| pyflate                          | 222 ms                                                         | 180 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 814 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 858 us: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| docutils                         | 1.05 sec                                                       | 947 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 170 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 123 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.9 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.91 ms: 1.07x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 34.9 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 276 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 174 ms: 1.06x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                   |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.70 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 924 ns: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.3 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 635 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 97.2 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.02x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.99 us: 1.03x slower                                                   |
| nbody                            | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                   |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.6 ms: 1.15x slower                                                   |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 149 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 100 ms: 3.47x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                            |

Benchmark hidden because not significant (4): dask, thrift, pycparser, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x