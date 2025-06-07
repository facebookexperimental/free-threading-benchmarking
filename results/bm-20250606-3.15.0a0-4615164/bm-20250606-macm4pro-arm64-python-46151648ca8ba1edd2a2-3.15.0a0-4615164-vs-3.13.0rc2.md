# Results vs. 3.13.0rc2

- fork: python
- ref: 46151648ca8ba1edd2a2
- machine: darwin-arm64
- commit hash: 4615164
- commit date: 2025-06-06
- overall geometric mean: 1.034x faster
- HPT reliability: 98.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.7 us: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 512 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 949 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 921 us: 1.08x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.7 us: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.7 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| regex_compile                    | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.11 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.8 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.8 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 711 ms: 1.09x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                   |
| nbody                            | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.61 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): richards_super, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250606-3.15.0a0-4615164/bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 98.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x