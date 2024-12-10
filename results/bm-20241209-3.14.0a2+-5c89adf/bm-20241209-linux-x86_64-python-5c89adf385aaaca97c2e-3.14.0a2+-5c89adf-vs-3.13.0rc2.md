# Results vs. 3.13.0rc2

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.57 sec: 1.12x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 825 ms: 1.68x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 892 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 479 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 367 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 675 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 671 ms: 1.27x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 28.4 ms: 1.09x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| async_generators           | 567 ms                                                       | 541 ms: 1.05x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 157 ms: 1.16x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| regex_dna      | 282 ms                                                       | 297 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 143 ms: 1.24x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.59 sec: 1.07x faster                                                 |
| xml_etree_generate  | 122 ms                                                       | 117 ms: 1.05x faster                                                   |
| json_dumps          | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_process, unpickle_pure_python, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 25.9 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 63.1 ms: 1.14x faster                                                  |
| genshi_text     | 31.7 ms                                                      | 30.3 ms: 1.04x faster                                                  |
| django_template | 44.3 ms                                                      | 46.6 ms: 1.05x slower                                                  |
| mako            | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 825 ms: 1.68x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 892 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 479 ms: 1.48x faster                                                   |
| deepcopy                   | 498 us                                                       | 345 us: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 367 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 675 ms: 1.32x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.7 us: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 671 ms: 1.27x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 143 ms: 1.24x faster                                                   |
| pylint                     | 470 ms                                                       | 392 ms: 1.20x faster                                                   |
| go                         | 191 ms                                                       | 160 ms: 1.19x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 26.1 ms: 1.16x faster                                                  |
| regex_compile              | 182 ms                                                       | 157 ms: 1.16x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.6 ms: 1.15x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 63.1 ms: 1.14x faster                                                  |
| spectral_norm              | 157 ms                                                       | 139 ms: 1.13x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.60 sec: 1.12x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.57 sec: 1.12x faster                                                 |
| meteor_contest             | 150 ms                                                       | 135 ms: 1.11x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.70 us: 1.11x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 204 us: 1.11x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 28.4 ms: 1.09x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 27.5 ms: 1.09x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.50 sec: 1.09x faster                                                 |
| sympy_str                  | 379 ms                                                       | 349 ms: 1.09x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 194 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.69 us: 1.08x faster                                                  |
| fannkuch                   | 547 ms                                                       | 510 ms: 1.07x faster                                                   |
| scimark_sor                | 179 ms                                                       | 167 ms: 1.07x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.59 sec: 1.07x faster                                                 |
| thrift                     | 1.10 ms                                                      | 1.03 ms: 1.07x faster                                                  |
| nqueens                    | 112 ms                                                       | 104 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 928 ms: 1.06x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.70 us: 1.06x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 94.6 ms: 1.06x faster                                                  |
| logging_simple             | 8.56 us                                                      | 8.09 us: 1.06x faster                                                  |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| comprehensions             | 22.2 us                                                      | 21.1 us: 1.05x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 1.67 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| async_generators           | 567 ms                                                       | 541 ms: 1.05x faster                                                   |
| sympy_expand               | 601 ms                                                       | 573 ms: 1.05x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 117 ms: 1.05x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 30.3 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.50 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 87.4 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.89 sec: 1.03x faster                                                 |
| pyflate                    | 664 ms                                                       | 684 ms: 1.03x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 98.0 ms: 1.05x slower                                                  |
| django_template            | 44.3 ms                                                      | 46.6 ms: 1.05x slower                                                  |
| regex_dna                  | 282 ms                                                       | 297 ms: 1.05x slower                                                   |
| mako                       | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| logging_silent             | 130 ns                                                       | 143 ns: 1.10x slower                                                   |
| python_startup             | 22.4 ms                                                      | 25.9 ms: 1.15x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.17 ms: 1.32x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.78 ms: 1.36x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 84.3 ms: 4.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (25): bench_thread_pool, chaos, xml_etree_process, sqlglot_optimize, sqlglot_transpile, richards, 2to3, float, pycparser, sqlglot_normalize, unpickle_pure_python, deltablue, scimark_fft, raytrace, python_startup_no_site, json, json_loads, regex_v8, generators, hexiom, scimark_lu, coverage, nbody, richards_super, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x