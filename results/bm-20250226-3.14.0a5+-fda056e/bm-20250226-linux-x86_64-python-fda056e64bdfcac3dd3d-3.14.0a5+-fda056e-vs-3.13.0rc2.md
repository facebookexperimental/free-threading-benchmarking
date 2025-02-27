# Results vs. 3.13.0rc2

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 842 ms: 1.65x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 887 ms: 1.58x faster                                                   |
| async_tree_none            | 572 ms                                                       | 379 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 476 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 485 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 687 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 680 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 434 ms: 1.16x faster                                                   |
| async_generators           | 567 ms                                                       | 504 ms: 1.13x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 98.7 ms: 1.17x faster                                                  |
| pidigits       | 251 ms                                                       | 229 ms: 1.10x faster                                                   |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.03 ms: 1.17x faster                                                  |
| regex_compile  | 182 ms                                                       | 160 ms: 1.14x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 31.4 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 157 ms: 1.12x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.57 sec: 1.08x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 306 us: 1.06x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| json_loads           | 34.3 us                                                      | 37.3 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 27.4 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 27.2 ms: 1.16x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 67.7 ms: 1.06x faster                                                  |
| mako            | 15.9 ms                                                      | 15.0 ms: 1.06x faster                                                  |
| django_template | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 842 ms: 1.65x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 887 ms: 1.58x faster                                                   |
| deepcopy                   | 498 us                                                       | 329 us: 1.51x faster                                                   |
| async_tree_none            | 572 ms                                                       | 379 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 476 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 485 ms: 1.38x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 36.8 us: 1.36x faster                                                  |
| go                         | 191 ms                                                       | 145 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 687 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 680 ms: 1.25x faster                                                   |
| spectral_norm              | 157 ms                                                       | 127 ms: 1.23x faster                                                   |
| pylint                     | 470 ms                                                       | 389 ms: 1.21x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.03 ms: 1.17x faster                                                  |
| float                      | 116 ms                                                       | 98.7 ms: 1.17x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 27.2 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 434 ms: 1.16x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.57 us: 1.15x faster                                                  |
| richards                   | 65.5 ms                                                      | 57.7 ms: 1.14x faster                                                  |
| regex_compile              | 182 ms                                                       | 160 ms: 1.14x faster                                                   |
| scimark_fft                | 473 ms                                                       | 418 ms: 1.13x faster                                                   |
| async_generators           | 567 ms                                                       | 504 ms: 1.13x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 157 ms: 1.12x faster                                                   |
| scimark_sor                | 179 ms                                                       | 160 ms: 1.12x faster                                                   |
| meteor_contest             | 150 ms                                                       | 135 ms: 1.11x faster                                                   |
| telco                      | 12.2 ms                                                      | 11.0 ms: 1.10x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| thrift                     | 1.10 ms                                                      | 998 us: 1.10x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 27.5 ms: 1.10x faster                                                  |
| richards_super             | 73.2 ms                                                      | 66.6 ms: 1.10x faster                                                  |
| pidigits                   | 251 ms                                                       | 229 ms: 1.10x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.66 us: 1.09x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 83.2 ms: 1.09x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                 |
| sympy_str                  | 379 ms                                                       | 349 ms: 1.09x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.57 sec: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.25 ms: 1.08x faster                                                  |
| pyflate                    | 664 ms                                                       | 616 ms: 1.08x faster                                                   |
| fannkuch                   | 547 ms                                                       | 509 ms: 1.07x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.47 sec: 1.07x faster                                                 |
| genshi_xml                 | 72.1 ms                                                      | 67.7 ms: 1.06x faster                                                  |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| mako                       | 15.9 ms                                                      | 15.0 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 213 us: 1.06x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.93 sec: 1.06x faster                                                 |
| chaos                      | 83.6 ms                                                      | 78.9 ms: 1.06x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                   |
| sqlglot_normalize          | 140 ms                                                       | 132 ms: 1.06x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| deltablue                  | 4.44 ms                                                      | 4.20 ms: 1.06x faster                                                  |
| nqueens                    | 112 ms                                                       | 106 ms: 1.05x faster                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 71.2 ms: 1.05x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 31.4 ms: 1.05x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.64 sec: 1.04x faster                                                 |
| pprint_pformat             | 1.94 sec                                                     | 1.87 sec: 1.04x faster                                                 |
| pprint_safe_repr           | 987 ms                                                       | 952 ms: 1.04x faster                                                   |
| logging_silent             | 130 ns                                                       | 136 ns: 1.04x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 306 us: 1.06x slower                                                   |
| logging_format             | 9.24 us                                                      | 9.79 us: 1.06x slower                                                  |
| coverage                   | 107 ms                                                       | 114 ms: 1.06x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| json_loads                 | 34.3 us                                                      | 37.3 us: 1.09x slower                                                  |
| django_template            | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.20 ms: 1.11x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 168 ms: 1.15x slower                                                   |
| json                       | 6.51 ms                                                      | 7.89 ms: 1.21x slower                                                  |
| python_startup             | 22.4 ms                                                      | 27.4 ms: 1.22x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.25 ms: 1.45x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.00 ms: 1.66x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.4 ms: 5.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (19): logging_simple, xml_etree_parse, xml_etree_process, crypto_pyaes, 2to3, generators, comprehensions, coroutines, sympy_expand, sqlglot_parse, pathlib, raytrace, sqlglot_transpile, nbody, regex_dna, pickle_pure_python, hexiom, python_startup_no_site, dulwich_log
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x