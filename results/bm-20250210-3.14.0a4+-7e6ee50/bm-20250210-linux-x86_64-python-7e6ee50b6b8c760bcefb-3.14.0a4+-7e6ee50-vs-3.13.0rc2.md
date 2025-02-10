# Results vs. 3.13.0rc2

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.78 sec: 1.06x faster                                                 |
| html5lib       | 92.6 ms                                                      | 83.0 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 862 ms: 1.61x faster                                                   |
| async_tree_none            | 572 ms                                                       | 373 ms: 1.53x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 919 ms: 1.53x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 461 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 661 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 690 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 394 ms: 1.28x faster                                                   |
| async_generators           | 567 ms                                                       | 500 ms: 1.13x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 123 ms: 1.06x slower                                                   |
| nbody          | 119 ms                                                       | 134 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 165 ms: 1.11x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.28 ms: 1.11x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 202 ms: 1.14x faster                                                   |
| xml_etree_process    | 85.9 ms                                                      | 75.9 ms: 1.13x faster                                                  |
| xml_etree_iterparse  | 177 ms                                                       | 162 ms: 1.10x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.55 sec: 1.09x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 116 ms: 1.05x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 281 us: 1.03x faster                                                   |
| json_loads           | 34.3 us                                                      | 37.0 us: 1.08x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.3 ms: 1.06x slower                                                  |
| python_startup         | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 29.3 ms: 1.08x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 67.7 ms: 1.06x faster                                                  |
| django_template | 44.3 ms                                                      | 46.8 ms: 1.06x slower                                                  |
| mako            | 15.9 ms                                                      | 17.5 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 862 ms: 1.61x faster                                                   |
| async_tree_none            | 572 ms                                                       | 373 ms: 1.53x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 919 ms: 1.53x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                   |
| deepcopy                   | 498 us                                                       | 335 us: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 461 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 661 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 690 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 394 ms: 1.28x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 39.5 us: 1.27x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.59 ms: 1.27x faster                                                  |
| spectral_norm              | 157 ms                                                       | 125 ms: 1.25x faster                                                   |
| go                         | 191 ms                                                       | 155 ms: 1.23x faster                                                   |
| scimark_sor                | 179 ms                                                       | 147 ms: 1.21x faster                                                   |
| pylint                     | 470 ms                                                       | 390 ms: 1.21x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 202 ms: 1.14x faster                                                   |
| async_generators           | 567 ms                                                       | 500 ms: 1.13x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 75.9 ms: 1.13x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.0 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.61 sec: 1.12x faster                                                 |
| richards                   | 65.5 ms                                                      | 58.6 ms: 1.12x faster                                                  |
| fannkuch                   | 547 ms                                                       | 489 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.05 ms: 1.12x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 83.0 ms: 1.12x faster                                                  |
| regex_compile              | 182 ms                                                       | 165 ms: 1.11x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.28 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 162 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 82.8 ms: 1.09x faster                                                  |
| richards_super             | 73.2 ms                                                      | 67.0 ms: 1.09x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.55 sec: 1.09x faster                                                 |
| chaos                      | 83.6 ms                                                      | 77.0 ms: 1.09x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 92.5 ms: 1.08x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 29.3 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 915 ms: 1.08x faster                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 69.7 ms: 1.07x faster                                                  |
| nqueens                    | 112 ms                                                       | 104 ms: 1.07x faster                                                   |
| typing_runtime_protocols   | 226 us                                                       | 211 us: 1.07x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 67.7 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.85 us: 1.06x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.78 sec: 1.06x faster                                                 |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| scimark_fft                | 473 ms                                                       | 447 ms: 1.06x faster                                                   |
| logging_simple             | 8.56 us                                                      | 8.10 us: 1.06x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.05x faster                                                   |
| comprehensions             | 22.2 us                                                      | 21.1 us: 1.05x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 28.5 ms: 1.05x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 4.23 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.85 sec: 1.05x faster                                                 |
| sympy_str                  | 379 ms                                                       | 362 ms: 1.05x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.50 sec: 1.04x faster                                                 |
| mdp                        | 3.80 sec                                                     | 3.65 sec: 1.04x faster                                                 |
| unpickle_pure_python       | 290 us                                                       | 281 us: 1.03x faster                                                   |
| raytrace                   | 344 ms                                                       | 358 ms: 1.04x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 147 ms: 1.05x slower                                                   |
| django_template            | 44.3 ms                                                      | 46.8 ms: 1.06x slower                                                  |
| json                       | 6.51 ms                                                      | 6.91 ms: 1.06x slower                                                  |
| float                      | 116 ms                                                       | 123 ms: 1.06x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 16.3 ms: 1.06x slower                                                  |
| logging_silent             | 130 ns                                                       | 140 ns: 1.07x slower                                                   |
| json_loads                 | 34.3 us                                                      | 37.0 us: 1.08x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 102 ms: 1.09x slower                                                   |
| mako                       | 15.9 ms                                                      | 17.5 ms: 1.10x slower                                                  |
| coverage                   | 107 ms                                                       | 118 ms: 1.10x slower                                                   |
| nbody                      | 119 ms                                                       | 134 ms: 1.13x slower                                                   |
| python_startup             | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.20 ms: 1.44x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.71 ms: 1.54x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 91.4 ms: 4.89x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (17): pidigits, bench_thread_pool, thrift, sqlglot_transpile, meteor_contest, regex_dna, sqlite_synth, coroutines, 2to3, hexiom, logging_format, sympy_expand, pyflate, scimark_lu, generators, sqlglot_parse, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x