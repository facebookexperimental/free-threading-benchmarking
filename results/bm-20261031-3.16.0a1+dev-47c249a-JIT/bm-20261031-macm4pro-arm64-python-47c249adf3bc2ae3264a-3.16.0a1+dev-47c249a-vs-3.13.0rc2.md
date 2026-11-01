# Results vs. 3.13.0rc2

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.253x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 854 ms: 1.23x faster                                                        |
| html5lib       | 23.1 ms                                                        | 17.5 ms: 1.32x faster                                                       |
| sphinx         | 409 ms                                                         | 373 ms: 1.10x faster                                                        |
| Geometric mean | (ref)                                                          | 1.16x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 105 ms: 1.84x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.59x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 97.7 ms: 1.46x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 35.7 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.67 ms: 1.11x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.06x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 21.7 ms: 1.45x faster                                                       |
| nbody          | 42.5 ms                                                        | 30.8 ms: 1.38x faster                                                       |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.28x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.91 ms: 1.20x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.3 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 610 ms: 1.64x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.31 ms: 1.41x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 72.6 us: 1.37x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 108 us: 1.20x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 21.5 ms: 1.18x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 32.0 ms: 1.12x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.1 us: 1.07x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                       |
| Geometric mean       | (ref)                                                          | 1.23x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.18 ms: 1.06x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.70 ms: 1.19x faster                                                       |
| django_template | 12.5 ms                                                        | 12.1 ms: 1.03x faster                                                       |
| Geometric mean  | (ref)                                                          | 1.11x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| richards                         | 22.1 ms                                                        | 9.46 ms: 2.33x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 10.8 ms: 2.29x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                        |
| pylint                           | 106 ms                                                         | 49.1 ms: 2.15x faster                                                       |
| mdp                              | 1.06 sec                                                       | 494 ms: 2.14x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 31.3 ms: 2.04x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 105 ms: 1.84x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.44 ms: 1.82x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 9.60 us: 1.71x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 610 ms: 1.64x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 611 us: 1.63x faster                                                        |
| deepcopy                         | 145 us                                                         | 89.3 us: 1.63x faster                                                       |
| k_core                           | 1.46 sec                                                       | 917 ms: 1.60x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 40.6 us: 1.59x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 256 ms: 1.59x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                        |
| go                               | 72.6 ms                                                        | 46.6 ms: 1.56x faster                                                       |
| pyflate                          | 222 ms                                                         | 148 ms: 1.50x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 97.7 ms: 1.46x faster                                                       |
| float                            | 31.4 ms                                                        | 21.7 ms: 1.45x faster                                                       |
| scimark_lu                       | 42.8 ms                                                        | 29.8 ms: 1.43x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.31 ms: 1.41x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 31.3 ms: 1.40x faster                                                       |
| nbody                            | 42.5 ms                                                        | 30.8 ms: 1.38x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 72.6 us: 1.37x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 90.9 ms: 1.36x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 960 ns: 1.35x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.68 us: 1.33x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 17.5 ms: 1.32x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 243 ms: 1.32x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                        |
| logging_format                   | 2.45 us                                                        | 1.86 us: 1.32x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 501 ms: 1.30x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.1 ms: 1.29x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.13 ms: 1.29x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 5.31 us: 1.28x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 29.8 ms: 1.25x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.29 ms: 1.25x faster                                                       |
| fannkuch                         | 179 ms                                                         | 144 ms: 1.24x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                        |
| docutils                         | 1.05 sec                                                       | 854 ms: 1.23x faster                                                        |
| chaos                            | 24.3 ms                                                        | 19.8 ms: 1.22x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.52 ms: 1.22x faster                                                       |
| logging_silent                   | 40.6 ns                                                        | 33.4 ns: 1.21x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.35 ms: 1.21x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 35.7 ms: 1.21x faster                                                       |
| pickle_pure_python               | 130 us                                                         | 108 us: 1.20x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.77 sec: 1.20x faster                                                      |
| regex_v8                         | 10.7 ms                                                        | 8.91 ms: 1.20x faster                                                       |
| mako                             | 4.41 ms                                                        | 3.70 ms: 1.19x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 16.8 ms: 1.18x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 21.5 ms: 1.18x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.74 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 32.0 ms: 1.12x faster                                                       |
| raytrace                         | 109 ms                                                         | 97.6 ms: 1.12x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.67 ms: 1.11x faster                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 30.2 ms: 1.11x faster                                                       |
| sphinx                           | 409 ms                                                         | 373 ms: 1.10x faster                                                        |
| thrift                           | 309 us                                                         | 282 us: 1.09x faster                                                        |
| json                             | 1.94 ms                                                        | 1.77 ms: 1.09x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.63 ms: 1.09x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 43.9 ms: 1.09x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.2 ms: 1.09x faster                                                       |
| many_optionals                   | 200 us                                                         | 185 us: 1.08x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.1 us: 1.07x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 88.3 ms: 1.07x faster                                                       |
| sympy_sum                        | 52.3 ms                                                        | 48.9 ms: 1.07x faster                                                       |
| regex_compile                    | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.06x faster                                                        |
| pycparser                        | 470 ms                                                         | 442 ms: 1.06x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.10 ms: 1.06x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.18 ms: 1.06x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 902 ns: 1.05x faster                                                        |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| django_template                  | 12.5 ms                                                        | 12.1 ms: 1.03x faster                                                       |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| sympy_str                        | 95.5 ms                                                        | 92.9 ms: 1.03x faster                                                       |
| sympy_expand                     | 159 ms                                                         | 155 ms: 1.03x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.0 ms: 3.01x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                                |

Benchmark hidden because not significant (1): 2to3
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a-JIT/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.253x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.15x