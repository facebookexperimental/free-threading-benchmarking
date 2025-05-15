# Results vs. 3.13.0rc2

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: darwin-arm64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.014x faster
- HPT reliability: 51.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 952 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.62 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.6 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.13 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 531 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| go                               | 72.6 ms                                                        | 57.7 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.2 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 929 us: 1.07x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 952 ms: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.62 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| richards                         | 22.1 ms                                                        | 22.2 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| sqlite_synth                     | 948 ns                                                         | 954 ns: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.61 ms: 1.01x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.0 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.0 us: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.13 ms: 1.03x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.6 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 498 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.78 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.8 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.6 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.1 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.4 ms: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.82 us: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.91 us: 1.16x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.61 us: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.4 ms: 1.19x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.73 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 51.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x