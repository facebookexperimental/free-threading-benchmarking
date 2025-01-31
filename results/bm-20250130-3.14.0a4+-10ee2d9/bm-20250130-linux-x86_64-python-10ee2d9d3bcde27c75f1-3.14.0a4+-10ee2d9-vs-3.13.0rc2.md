# Results vs. 3.13.0rc2

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.049x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 468 ms: 1.05x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.71 sec: 1.08x faster                                                 |
| html5lib       | 92.6 ms                                                      | 85.9 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 888 ms: 1.56x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 452 ms: 1.48x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 958 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 526 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 679 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 727 ms: 1.17x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| async_generators           | 567 ms                                                       | 546 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 101 ms: 1.15x faster                                                   |
| pidigits       | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                       | 127 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.46 ms: 1.06x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| xml_etree_iterparse  | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.52 sec: 1.10x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 117 ms: 1.05x faster                                                   |
| json_loads           | 34.3 us                                                      | 37.6 us: 1.10x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 322 us: 1.11x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 15.9 ms: 1.04x slower                                                  |
| python_startup         | 22.4 ms                                                      | 26.6 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                  |
| mako            | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 76.1 ms: 1.06x slower                                                  |
| django_template | 44.3 ms                                                      | 49.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 888 ms: 1.56x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 452 ms: 1.48x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 958 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 526 ms: 1.35x faster                                                   |
| deepcopy                   | 498 us                                                       | 371 us: 1.34x faster                                                   |
| spectral_norm              | 157 ms                                                       | 119 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 679 ms: 1.31x faster                                                   |
| go                         | 191 ms                                                       | 151 ms: 1.27x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.1 ms: 1.20x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 42.8 us: 1.17x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 727 ms: 1.17x faster                                                   |
| pylint                     | 470 ms                                                       | 409 ms: 1.15x faster                                                   |
| float                      | 116 ms                                                       | 101 ms: 1.15x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| scimark_sor                | 179 ms                                                       | 160 ms: 1.12x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 89.7 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.64 sec: 1.11x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.70 us: 1.11x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.52 sec: 1.10x faster                                                 |
| pyflate                    | 664 ms                                                       | 602 ms: 1.10x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.49 sec: 1.09x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.71 sec: 1.08x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 85.9 ms: 1.08x faster                                                  |
| scimark_fft                | 473 ms                                                       | 442 ms: 1.07x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 28.3 ms: 1.07x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.76 us: 1.06x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.46 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.41 ms: 1.05x faster                                                  |
| richards                   | 65.5 ms                                                      | 62.3 ms: 1.05x faster                                                  |
| pidigits                   | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 941 ms: 1.05x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 117 ms: 1.05x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| thrift                     | 1.10 ms                                                      | 1.06 ms: 1.04x faster                                                  |
| async_generators           | 567 ms                                                       | 546 ms: 1.04x faster                                                   |
| generators                 | 40.0 ms                                                      | 38.5 ms: 1.04x faster                                                  |
| richards_super             | 73.2 ms                                                      | 75.9 ms: 1.04x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 15.9 ms: 1.04x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| mako                       | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                  |
| 2to3                       | 445 ms                                                       | 468 ms: 1.05x slower                                                   |
| raytrace                   | 344 ms                                                       | 362 ms: 1.05x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 76.1 ms: 1.06x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 100 ms: 1.07x slower                                                   |
| nbody                      | 119 ms                                                       | 127 ms: 1.07x slower                                                   |
| json_loads                 | 34.3 us                                                      | 37.6 us: 1.10x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 154 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 322 us: 1.11x slower                                                   |
| django_template            | 44.3 ms                                                      | 49.2 ms: 1.11x slower                                                  |
| coverage                   | 107 ms                                                       | 119 ms: 1.11x slower                                                   |
| logging_silent             | 130 ns                                                       | 147 ns: 1.13x slower                                                   |
| json                       | 6.51 ms                                                      | 7.38 ms: 1.13x slower                                                  |
| python_startup             | 22.4 ms                                                      | 26.6 ms: 1.19x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.1 us: 1.20x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.56 ms: 1.33x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.75 ms: 1.55x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 100.0 ms: 5.35x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (26): regex_compile, chaos, sqlglot_parse, typing_runtime_protocols, regex_dna, pathlib, nqueens, xml_etree_process, pprint_pformat, sqlglot_optimize, sympy_expand, fannkuch, scimark_lu, bench_thread_pool, pycparser, coroutines, comprehensions, scimark_monte_carlo, deltablue, sympy_str, meteor_contest, logging_simple, pickle_pure_python, hexiom, sympy_sum, sqlglot_transpile
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.12x