# Results vs. 3.13.0rc2

- fork: python
- ref: f57be7b2b3dc61ed18c5
- machine: darwin-arm64
- commit hash: f57be7b
- commit date: 2025-08-24
- overall geometric mean: 1.032x faster
- HPT reliability: 98.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.5 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 31.2 ms: 1.01x faster                                                   |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads         | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_process   | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| json_loads          | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse     | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 145 us: 1.11x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.77 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 529 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| go                               | 72.6 ms                                                        | 55.6 ms: 1.30x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.78 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 915 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 923 us: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.3 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.77 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 63.4 us: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.0 ns: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                   |
| float                            | 31.4 ms                                                        | 31.2 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.00x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.2 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 312 us: 1.55x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.0 ms: 2.71x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.5 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (5): genshi_xml, thrift, unpickle_pure_python, sqlite_synth, regex_compile
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 98.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x