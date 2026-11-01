# Results vs. 3.13.0rc2

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.123x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 887 ms: 1.18x faster                                                        |
| html5lib       | 23.1 ms                                                        | 19.9 ms: 1.16x faster                                                       |
| sphinx         | 409 ms                                                         | 380 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.6 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.64 ms: 1.12x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                       |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| nbody          | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.97 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.4 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.52 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 797 ms: 1.25x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.6 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.12 ms: 1.06x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.32 ms: 1.02x faster                                                       |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pylint                           | 106 ms                                                         | 49.6 ms: 2.13x faster                                                       |
| mdp                              | 1.06 sec                                                       | 498 ms: 2.12x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.6 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.88 ms: 1.62x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 617 us: 1.61x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.0 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 966 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 45.3 us: 1.43x faster                                                       |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.42x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.52 ms: 1.32x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 797 ms: 1.25x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 178 ms: 1.25x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 8.97 ms: 1.19x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.73 ms: 1.18x faster                                                       |
| docutils                         | 1.05 sec                                                       | 887 ms: 1.18x faster                                                        |
| float                            | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 19.9 ms: 1.16x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 108 ms: 1.14x faster                                                        |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.3 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                      |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| richards                         | 22.1 ms                                                        | 19.7 ms: 1.12x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.64 ms: 1.12x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.57 ms: 1.11x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 34.1 ms: 1.09x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 40.5 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.6 us: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 380 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 88.4 ms: 1.07x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.06x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.12 ms: 1.06x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.11 us: 1.06x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.16 ms: 1.05x faster                                                       |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.05x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 621 ms: 1.05x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.52 us: 1.04x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 912 ns: 1.04x faster                                                        |
| thrift                           | 309 us                                                         | 298 us: 1.04x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| pycparser                        | 470 ms                                                         | 456 ms: 1.03x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| mako                             | 4.41 ms                                                        | 4.32 ms: 1.02x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                       |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.2 ms: 1.00x faster                                                       |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 97.0 ms: 1.02x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.03x slower                                                        |
| nbody                            | 42.5 ms                                                        | 44.2 ms: 1.04x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                       |
| generators                       | 15.7 ms                                                        | 16.7 ms: 1.07x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 45.7 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.0 ms: 1.07x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                       |
| many_optionals                   | 200 us                                                         | 220 us: 1.10x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmark hidden because not significant (1): shortest_path
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.123x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.10x