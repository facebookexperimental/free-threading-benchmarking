# Results vs. 3.13.0rc2

- fork: python
- ref: 1a0edb1fa899c067f19b
- machine: darwin-arm64
- commit hash: 1a0edb1
- commit date: 2026-04-09
- overall geometric mean: 1.022x faster
- HPT reliability: 63.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.5 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.1 ms: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 788 us: 2.59x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 512 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 780 ns: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 56.1 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.1 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.3 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.5 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.1 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.5 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 244 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.28 us: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.4 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.1 ms: 1.29x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.30 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.0 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.32x slower                                                    |
| many_optionals                   | 200 us                                                         | 266 us: 1.33x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260409-3.15.0a8+-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 63.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x