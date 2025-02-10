# Results vs. 3.12.6

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.78 sec: 1.06x faster                                                 |
| html5lib       | 88.9 ms                                                | 83.0 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 862 ms: 2.14x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 919 ms: 2.11x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.09x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 461 ms: 2.02x faster                                                   |
| async_tree_none            | 741 ms                                                 | 373 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 394 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 661 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 690 ms: 1.56x faster                                                   |
| async_generators           | 589 ms                                                 | 500 ms: 1.18x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.63x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 134 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.28 ms: 1.20x faster                                                  |
| regex_compile  | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 202 ms: 1.19x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.55 sec: 1.13x faster                                                 |
| xml_etree_process    | 83.7 ms                                                | 75.9 ms: 1.10x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 281 us: 1.06x faster                                                   |
| json_dumps           | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_iterparse, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                  |
| python_startup         | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 17.5 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): genshi_text, genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 862 ms: 2.14x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 919 ms: 2.11x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.09x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 461 ms: 2.02x faster                                                   |
| async_tree_none            | 741 ms                                                 | 373 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 394 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 661 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 690 ms: 1.56x faster                                                   |
| deepcopy                   | 468 us                                                 | 335 us: 1.40x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 39.5 us: 1.33x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.1 us: 1.28x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.77 ms: 1.26x faster                                                  |
| spectral_norm              | 156 ms                                                 | 125 ms: 1.24x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 177 ms: 1.23x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.28 ms: 1.20x faster                                                  |
| pylint                     | 465 ms                                                 | 390 ms: 1.19x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 202 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.50 sec: 1.19x faster                                                 |
| async_generators           | 589 ms                                                 | 500 ms: 1.18x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.61 sec: 1.17x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.10 us: 1.17x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 82.8 ms: 1.16x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 92.5 ms: 1.16x faster                                                  |
| raytrace                   | 408 ms                                                 | 358 ms: 1.14x faster                                                   |
| regex_compile              | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.55 sec: 1.13x faster                                                 |
| scimark_sor                | 167 ms                                                 | 147 ms: 1.13x faster                                                   |
| nqueens                    | 117 ms                                                 | 104 ms: 1.12x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| scimark_fft                | 500 ms                                                 | 447 ms: 1.12x faster                                                   |
| pathlib                    | 31.6 ms                                                | 28.5 ms: 1.11x faster                                                  |
| go                         | 172 ms                                                 | 155 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.05 ms: 1.11x faster                                                  |
| fannkuch                   | 540 ms                                                 | 489 ms: 1.10x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 75.9 ms: 1.10x faster                                                  |
| chaos                      | 84.9 ms                                                | 77.0 ms: 1.10x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 27.0 ms: 1.10x faster                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.13 ms: 1.10x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| pyflate                    | 727 ms                                                 | 667 ms: 1.09x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 69.7 ms: 1.09x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.65 sec: 1.09x faster                                                 |
| richards_super             | 72.8 ms                                                | 67.0 ms: 1.09x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                  |
| html5lib                   | 88.9 ms                                                | 83.0 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.85 sec: 1.07x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 147 ms: 1.07x faster                                                   |
| unpickle_pure_python       | 300 us                                                 | 281 us: 1.06x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 211 us: 1.06x faster                                                   |
| sympy_str                  | 385 ms                                                 | 362 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 915 ms: 1.06x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.78 sec: 1.06x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.85 us: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| scimark_lu                 | 152 ms                                                 | 148 ms: 1.03x faster                                                   |
| sympy_expand               | 582 ms                                                 | 603 ms: 1.04x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| mako                       | 15.7 ms                                                | 17.5 ms: 1.11x slower                                                  |
| nbody                      | 119 ms                                                 | 134 ms: 1.13x slower                                                   |
| python_startup             | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                  |
| coverage                   | 95.4 ms                                                | 118 ms: 1.24x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.20 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.71 ms: 1.91x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 91.4 ms: 4.41x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (24): xml_etree_iterparse, 2to3, sqlalchemy_imperative, logging_format, genshi_text, richards, json_loads, hexiom, generators, pickle_pure_python, regex_dna, deltablue, meteor_contest, telco, float, genshi_xml, thrift, logging_silent, sqlglot_parse, sqlite_synth, json, dulwich_log, coroutines, django_template
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x