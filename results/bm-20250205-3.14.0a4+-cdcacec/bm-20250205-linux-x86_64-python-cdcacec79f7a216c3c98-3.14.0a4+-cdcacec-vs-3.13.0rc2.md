# Results vs. 3.13.0rc2

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 470 ms: 1.06x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 92.6 ms                                                      | 78.4 ms: 1.18x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 902 ms: 1.54x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 914 ms: 1.53x faster                                                   |
| async_tree_none            | 572 ms                                                       | 386 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 473 ms: 1.42x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 501 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 699 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 735 ms: 1.21x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 704 ms: 1.09x faster                                                   |
| async_generators           | 567 ms                                                       | 522 ms: 1.09x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 232 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 123 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 157 ms: 1.16x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.18 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 196 ms: 1.18x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.44 sec: 1.14x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| pickle_pure_python   | 416 us                                                       | 389 us: 1.07x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 271 us: 1.07x faster                                                   |
| xml_etree_process    | 85.9 ms                                                      | 80.8 ms: 1.06x faster                                                  |
| json_dumps           | 14.1 ms                                                      | 16.1 ms: 1.14x slower                                                  |
| json_loads           | 34.3 us                                                      | 39.6 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 26.7 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 28.1 ms: 1.13x faster                                                  |
| genshi_xml     | 72.1 ms                                                      | 68.4 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 902 ms: 1.54x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 914 ms: 1.53x faster                                                   |
| async_tree_none            | 572 ms                                                       | 386 ms: 1.48x faster                                                   |
| deepcopy                   | 498 us                                                       | 340 us: 1.46x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 473 ms: 1.42x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 501 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.32x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.6 us: 1.30x faster                                                  |
| go                         | 191 ms                                                       | 153 ms: 1.25x faster                                                   |
| spectral_norm              | 157 ms                                                       | 127 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 699 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.38 us: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 735 ms: 1.21x faster                                                   |
| pylint                     | 470 ms                                                       | 393 ms: 1.20x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 78.4 ms: 1.18x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 196 ms: 1.18x faster                                                   |
| regex_compile              | 182 ms                                                       | 157 ms: 1.16x faster                                                   |
| scimark_sor                | 179 ms                                                       | 155 ms: 1.15x faster                                                   |
| richards                   | 65.5 ms                                                      | 56.8 ms: 1.15x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.44 sec: 1.14x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 4.18 ms: 1.13x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.1 ms: 1.13x faster                                                  |
| richards_super             | 73.2 ms                                                      | 65.1 ms: 1.13x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.55 us: 1.12x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.60 sec: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.04 ms: 1.12x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.9 ms: 1.12x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 204 us: 1.10x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.39 us: 1.10x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 704 ms: 1.09x faster                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 68.7 ms: 1.09x faster                                                  |
| async_generators           | 567 ms                                                       | 522 ms: 1.09x faster                                                   |
| pidigits                   | 251 ms                                                       | 232 ms: 1.08x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 92.7 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 84.1 ms: 1.08x faster                                                  |
| meteor_contest             | 150 ms                                                       | 140 ms: 1.07x faster                                                   |
| sympy_str                  | 379 ms                                                       | 353 ms: 1.07x faster                                                   |
| comprehensions             | 22.2 us                                                      | 20.7 us: 1.07x faster                                                  |
| pickle_pure_python         | 416 us                                                       | 389 us: 1.07x faster                                                   |
| scimark_fft                | 473 ms                                                       | 442 ms: 1.07x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 271 us: 1.07x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.55 sec: 1.07x faster                                                 |
| chaos                      | 83.6 ms                                                      | 78.3 ms: 1.07x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 28.4 ms: 1.06x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 80.8 ms: 1.06x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 28.2 ms: 1.06x faster                                                  |
| pyflate                    | 664 ms                                                       | 628 ms: 1.06x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 68.4 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.86 sec: 1.05x faster                                                 |
| pprint_safe_repr           | 987 ms                                                       | 947 ms: 1.04x faster                                                   |
| fannkuch                   | 547 ms                                                       | 527 ms: 1.04x faster                                                   |
| nbody                      | 119 ms                                                       | 123 ms: 1.04x slower                                                   |
| 2to3                       | 445 ms                                                       | 470 ms: 1.06x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.14 us: 1.07x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 1.88 ms: 1.07x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.18 ms: 1.08x slower                                                  |
| json                       | 6.51 ms                                                      | 7.02 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 151 ms: 1.08x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 101 ms: 1.08x slower                                                   |
| coverage                   | 107 ms                                                       | 119 ms: 1.11x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.26 ms: 1.13x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.1 ms: 1.14x slower                                                  |
| json_loads                 | 34.3 us                                                      | 39.6 us: 1.15x slower                                                  |
| python_startup             | 22.4 ms                                                      | 26.7 ms: 1.19x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.83 ms: 1.55x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.81 ms: 1.58x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 97.0 ms: 5.19x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (19): xml_etree_iterparse, sqlglot_transpile, scimark_lu, deltablue, raytrace, float, regex_dna, sympy_expand, pycparser, logging_silent, coroutines, nqueens, hexiom, generators, django_template, python_startup_no_site, regex_v8, mako, sympy_sum
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x