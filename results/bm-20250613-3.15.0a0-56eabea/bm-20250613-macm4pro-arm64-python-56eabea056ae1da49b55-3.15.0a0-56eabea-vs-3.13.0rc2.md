# Results vs. 3.13.0rc2

- fork: python
- ref: 56eabea056ae1da49b55
- machine: darwin-arm64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.022x faster
- HPT reliability: 71.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 931 ms: 1.07x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.9 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 959 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.33x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 56.6 ms: 1.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 931 ms: 1.07x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.1 us: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 973 us: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.9 us: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.9 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.00x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                    |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.3 ms: 1.06x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.16 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.42 us: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 709 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.4 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 253 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.74 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.1 ms: 3.05x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 198 ns: 4.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (4): sympy_integrate, asyncio_websockets, regex_compile, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250613-3.15.0a0-56eabea/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 71.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x