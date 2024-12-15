# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 422 ms: 1.06x faster                                                 |
| docutils       | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                               |
| html5lib       | 92.6 ms                                                      | 84.4 ms: 1.10x faster                                                |
| Geometric mean | (ref)                                                        | 1.09x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 888 ms: 1.58x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 910 ms: 1.52x faster                                                 |
| async_tree_none            | 572 ms                                                       | 378 ms: 1.51x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 449 ms: 1.49x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 494 ms: 1.44x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 692 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 673 ms: 1.27x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                 |
| async_generators           | 567 ms                                                       | 538 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                         |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 107 ms: 1.08x faster                                                 |
| pidigits       | 251 ms                                                       | 240 ms: 1.05x faster                                                 |
| nbody          | 119 ms                                                       | 129 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                |
| regex_compile  | 182 ms                                                       | 167 ms: 1.09x faster                                                 |
| regex_dna      | 282 ms                                                       | 273 ms: 1.03x faster                                                 |
| regex_v8       | 32.8 ms                                                      | 31.8 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|---------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 136 ms: 1.30x faster                                                 |
| xml_etree_parse     | 231 ms                                                       | 195 ms: 1.18x faster                                                 |
| tomli_loads         | 2.78 sec                                                     | 2.51 sec: 1.11x faster                                               |
| xml_etree_generate  | 122 ms                                                       | 112 ms: 1.09x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                |
| pickle_pure_python  | 416 us                                                       | 446 us: 1.07x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.07x faster                                                         |

Benchmark hidden because not significant (3): xml_etree_process, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                |
| python_startup         | 22.4 ms                                                      | 24.7 ms: 1.10x slower                                                |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 65.3 ms: 1.10x faster                                                |
| genshi_text    | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                |
| mako           | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                        | 1.04x faster                                                         |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 888 ms: 1.58x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 910 ms: 1.52x faster                                                 |
| async_tree_none            | 572 ms                                                       | 378 ms: 1.51x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 449 ms: 1.49x faster                                                 |
| deepcopy                   | 498 us                                                       | 338 us: 1.47x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 494 ms: 1.44x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 136 ms: 1.30x faster                                                 |
| deepcopy_memo              | 50.1 us                                                      | 38.6 us: 1.30x faster                                                |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 692 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 673 ms: 1.27x faster                                                 |
| go                         | 191 ms                                                       | 153 ms: 1.25x faster                                                 |
| telco                      | 12.2 ms                                                      | 9.96 ms: 1.22x faster                                                |
| scimark_sor                | 179 ms                                                       | 149 ms: 1.20x faster                                                 |
| pylint                     | 470 ms                                                       | 392 ms: 1.20x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 195 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.51 us: 1.17x faster                                                |
| sympy_integrate            | 30.2 ms                                                      | 26.5 ms: 1.14x faster                                                |
| nqueens                    | 112 ms                                                       | 98.1 ms: 1.14x faster                                                |
| docutils                   | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                               |
| crypto_pyaes               | 100 ms                                                       | 89.1 ms: 1.12x faster                                                |
| regex_effbot               | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                |
| tomli_loads                | 2.78 sec                                                     | 2.51 sec: 1.11x faster                                               |
| genshi_xml                 | 72.1 ms                                                      | 65.3 ms: 1.10x faster                                                |
| genshi_text                | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                |
| spectral_norm              | 157 ms                                                       | 142 ms: 1.10x faster                                                 |
| meteor_contest             | 150 ms                                                       | 137 ms: 1.10x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 84.4 ms: 1.10x faster                                                |
| thrift                     | 1.10 ms                                                      | 1.00 ms: 1.10x faster                                                |
| xml_etree_generate         | 122 ms                                                       | 112 ms: 1.09x faster                                                 |
| regex_compile              | 182 ms                                                       | 167 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 5.77 sec: 1.09x faster                                               |
| fannkuch                   | 547 ms                                                       | 504 ms: 1.09x faster                                                 |
| float                      | 116 ms                                                       | 107 ms: 1.08x faster                                                 |
| richards_super             | 73.2 ms                                                      | 67.8 ms: 1.08x faster                                                |
| typing_runtime_protocols   | 226 us                                                       | 210 us: 1.07x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.74 us: 1.07x faster                                                |
| pprint_safe_repr           | 987 ms                                                       | 929 ms: 1.06x faster                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                |
| chaos                      | 83.6 ms                                                      | 79.0 ms: 1.06x faster                                                |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                 |
| 2to3                       | 445 ms                                                       | 422 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.40 ms: 1.05x faster                                                |
| async_generators           | 567 ms                                                       | 538 ms: 1.05x faster                                                 |
| pidigits                   | 251 ms                                                       | 240 ms: 1.05x faster                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 71.4 ms: 1.05x faster                                                |
| scimark_fft                | 473 ms                                                       | 453 ms: 1.05x faster                                                 |
| richards                   | 65.5 ms                                                      | 62.7 ms: 1.05x faster                                                |
| scimark_monte_carlo        | 90.6 ms                                                      | 86.7 ms: 1.05x faster                                                |
| sqlglot_parse              | 1.76 ms                                                      | 1.68 ms: 1.05x faster                                                |
| pprint_pformat             | 1.94 sec                                                     | 1.88 sec: 1.03x faster                                               |
| regex_dna                  | 282 ms                                                       | 273 ms: 1.03x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 31.8 ms: 1.03x faster                                                |
| logging_silent             | 130 ns                                                       | 135 ns: 1.04x slower                                                 |
| mako                       | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                |
| json_dumps                 | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                |
| pickle_pure_python         | 416 us                                                       | 446 us: 1.07x slower                                                 |
| nbody                      | 119 ms                                                       | 129 ms: 1.08x slower                                                 |
| python_startup             | 22.4 ms                                                      | 24.7 ms: 1.10x slower                                                |
| gc_traversal               | 5.70 ms                                                      | 7.01 ms: 1.23x slower                                                |
| create_gc_cycles           | 2.41 ms                                                      | 3.36 ms: 1.39x slower                                                |
| bench_mp_pool              | 18.7 ms                                                      | 90.9 ms: 4.87x slower                                                |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                         |

Benchmark hidden because not significant (26): pathlib, xml_etree_process, deltablue, sympy_sum, json, sympy_str, logging_format, sqlglot_transpile, coverage, pycparser, hexiom, json_loads, raytrace, sympy_expand, generators, comprehensions, unpickle_pure_python, logging_simple, coroutines, mdp, sqlglot_normalize, pyflate, django_template, dulwich_log, scimark_lu, bench_thread_pool
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x