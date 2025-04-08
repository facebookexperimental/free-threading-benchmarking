# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.000x faster
- HPT reliability: 90.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 511 ms: 1.15x slower                                                  |
| html5lib       | 92.6 ms                                                      | 99.3 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 703 ms: 1.99x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 793 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 316 ms: 1.59x faster                                                  |
| async_tree_none            | 572 ms                                                       | 368 ms: 1.56x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 451 ms: 1.49x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 495 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 617 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 650 ms: 1.37x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 36.6 ms: 1.19x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 100 ms: 1.15x faster                                                  |
| pidigits       | 251 ms                                                       | 231 ms: 1.09x faster                                                  |
| nbody          | 119 ms                                                       | 150 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                 |
| regex_compile  | 182 ms                                                       | 192 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 143 ms: 1.23x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 216 ms: 1.07x faster                                                  |
| tomli_loads          | 2.78 sec                                                     | 2.88 sec: 1.03x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 129 ms: 1.05x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 91.5 ms: 1.07x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 312 us: 1.08x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 497 us: 1.19x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                 |
| json_loads           | 34.3 us                                                      | 41.7 us: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                 |
| python_startup_no_site | 15.3 ms                                                      | 21.8 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 79.3 ms: 1.10x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 37.0 ms: 1.17x slower                                                 |
| django_template | 44.3 ms                                                      | 53.0 ms: 1.20x slower                                                 |
| mako            | 15.9 ms                                                      | 21.4 ms: 1.34x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 703 ms: 1.99x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 793 ms: 1.75x faster                                                  |
| mdp                        | 3.80 sec                                                     | 2.35 sec: 1.61x faster                                                |
| async_tree_none_tg         | 504 ms                                                       | 316 ms: 1.59x faster                                                  |
| async_tree_none            | 572 ms                                                       | 368 ms: 1.56x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 451 ms: 1.49x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 495 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 617 ms: 1.38x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 4.14 ms: 1.38x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 650 ms: 1.37x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 143 ms: 1.23x faster                                                  |
| deepcopy                   | 498 us                                                       | 405 us: 1.23x faster                                                  |
| float                      | 116 ms                                                       | 100 ms: 1.15x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                 |
| deepcopy_memo              | 50.1 us                                                      | 45.8 us: 1.09x faster                                                 |
| pidigits                   | 251 ms                                                       | 231 ms: 1.09x faster                                                  |
| pylint                     | 470 ms                                                       | 433 ms: 1.09x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 216 ms: 1.07x faster                                                  |
| go                         | 191 ms                                                       | 179 ms: 1.07x faster                                                  |
| spectral_norm              | 157 ms                                                       | 147 ms: 1.07x faster                                                  |
| scimark_sor                | 179 ms                                                       | 168 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.86 us: 1.06x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.79 us: 1.05x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.88 sec: 1.03x slower                                                |
| richards_super             | 73.2 ms                                                      | 76.1 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.03 sec: 1.04x slower                                                |
| xml_etree_generate         | 122 ms                                                       | 129 ms: 1.05x slower                                                  |
| regex_compile              | 182 ms                                                       | 192 ms: 1.05x slower                                                  |
| logging_silent             | 130 ns                                                       | 138 ns: 1.06x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 91.5 ms: 1.07x slower                                                 |
| pyflate                    | 664 ms                                                       | 711 ms: 1.07x slower                                                  |
| richards                   | 65.5 ms                                                      | 70.2 ms: 1.07x slower                                                 |
| html5lib                   | 92.6 ms                                                      | 99.3 ms: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.27 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 312 us: 1.08x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.27 us: 1.08x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 6.90 sec: 1.10x slower                                                |
| genshi_xml                 | 72.1 ms                                                      | 79.3 ms: 1.10x slower                                                 |
| json                       | 6.51 ms                                                      | 7.18 ms: 1.10x slower                                                 |
| fannkuch                   | 547 ms                                                       | 604 ms: 1.10x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 4.91 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 2.15 sec: 1.11x slower                                                |
| sympy_str                  | 379 ms                                                       | 426 ms: 1.12x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 113 ms: 1.13x slower                                                  |
| sympy_expand               | 601 ms                                                       | 680 ms: 1.13x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.3 us: 1.14x slower                                                 |
| 2to3                       | 445 ms                                                       | 511 ms: 1.15x slower                                                  |
| raytrace                   | 344 ms                                                       | 398 ms: 1.16x slower                                                  |
| logging_format             | 9.24 us                                                      | 10.7 us: 1.16x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 262 us: 1.16x slower                                                  |
| generators                 | 40.0 ms                                                      | 46.6 ms: 1.17x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 37.0 ms: 1.17x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 106 ms: 1.17x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 249 ms: 1.18x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 36.6 ms: 1.19x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 497 us: 1.19x slower                                                  |
| django_template            | 44.3 ms                                                      | 53.0 ms: 1.20x slower                                                 |
| meteor_contest             | 150 ms                                                       | 181 ms: 1.20x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.51 ms: 1.22x slower                                                 |
| json_loads                 | 34.3 us                                                      | 41.7 us: 1.22x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 183 ms: 1.25x slower                                                  |
| nbody                      | 119 ms                                                       | 150 ms: 1.27x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 10.6 ms: 1.31x slower                                                 |
| python_startup             | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                 |
| mako                       | 15.9 ms                                                      | 21.4 ms: 1.34x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 21.8 ms: 1.42x slower                                                 |
| coverage                   | 107 ms                                                       | 158 ms: 1.47x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 88.4 ms: 4.73x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (14): regex_v8, pycparser, asyncio_websockets, async_generators, telco, dulwich_log, sympy_integrate, docutils, nqueens, regex_dna, scimark_fft, create_gc_cycles, pathlib, chaos
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 90.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x