# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.095x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 902 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 387 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 281 ms: 1.86x faster                                                        |
| async_generators                 | 193 ms                                                         | 128 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 284 ms: 1.43x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 276 ms: 1.40x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.1 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 146 ms: 1.14x faster                                                        |
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                       |
| nbody          | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.00 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 814 ms: 1.23x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.0 ms: 1.13x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 93.2 us: 1.07x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 7.99 ms: 1.08x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                       |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pylint                           | 106 ms                                                         | 50.3 ms: 2.10x faster                                                       |
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 281 ms: 1.86x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 628 us: 1.58x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.98 ms: 1.57x faster                                                       |
| deepcopy                         | 145 us                                                         | 93.6 us: 1.55x faster                                                       |
| async_generators                 | 193 ms                                                         | 128 ms: 1.51x faster                                                        |
| k_core                           | 1.46 sec                                                       | 970 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 284 ms: 1.43x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.5 us: 1.42x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 276 ms: 1.40x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                       |
| go                               | 72.6 ms                                                        | 52.4 ms: 1.38x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.2 ms: 1.33x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.28x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 814 ms: 1.23x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.00 ms: 1.19x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.17x faster                                                        |
| docutils                         | 1.05 sec                                                       | 902 ms: 1.16x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.77 ms: 1.15x faster                                                       |
| pidigits                         | 166 ms                                                         | 146 ms: 1.14x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.0 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 271 ms: 1.11x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.1 ms: 1.10x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.09x faster                                                       |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 7.99 ms: 1.08x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 87.6 ms: 1.08x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 93.2 us: 1.07x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 35.2 ms: 1.06x faster                                                       |
| sphinx                           | 409 ms                                                         | 387 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 41.2 ms: 1.05x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.22 ms: 1.04x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                       |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 314 ms: 1.02x faster                                                        |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.78 us: 1.00x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                       |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.0 ms: 1.02x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 42.4 ns: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                       |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                        |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.28 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 36.5 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                       |
| nbody                            | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                       |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.1 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (6): pprint_pformat, json_loads, pycparser, logging_format, shortest_path, connected_components
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-CLANG/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x