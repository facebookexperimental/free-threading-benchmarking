# Results vs. 3.13.0rc2

- fork: python
- ref: 1857a40807daeae3a1bf
- machine: darwin-arm64
- commit hash: 1857a40
- commit date: 2026-01-14
- overall geometric mean: 1.004x faster
- HPT reliability: 75.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.0 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 904 ms: 1.11x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.97 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 825 us: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 521 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 604 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.18 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| go                               | 72.6 ms                                                        | 60.6 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 827 ns: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 904 ms: 1.11x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.6 ms: 1.05x slower                                                    |
| sphinx                           | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 686 ms: 1.06x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.8 ns: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.21 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.5 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.12x slower                                                     |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.97 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.1 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.9 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.37 us: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.2 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.1 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 549 us: 1.33x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 277 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 61.3 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.0 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a4+-1857a40-NOGIL/bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4+-1857a40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 75.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x