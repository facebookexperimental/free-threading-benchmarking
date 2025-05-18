# Results vs. 3.13.0rc2

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.021x faster
- HPT reliability: 89.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 26.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 960 ms: 1.04x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.0 us: 1.00x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 524 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 949 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| go                               | 72.6 ms                                                        | 57.0 ms: 1.27x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.4 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.99 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 929 us: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 214 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 960 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 318 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.9 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 645 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.0 us: 1.00x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.6 ms: 1.00x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| xml_etree_process                | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 66.2 us: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.2 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.7 ms: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.99 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.2 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.79 us: 1.14x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.74 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (8): genshi_text, telco, async_tree_eager_cpu_io_mixed, fannkuch, xml_etree_generate, sqlite_synth, json, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 89.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x