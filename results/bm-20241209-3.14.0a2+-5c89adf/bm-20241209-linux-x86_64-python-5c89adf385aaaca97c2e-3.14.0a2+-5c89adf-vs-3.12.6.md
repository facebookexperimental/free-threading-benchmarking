# Results vs. 3.12.6

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 433 ms: 1.05x faster                                                   |
| docutils       | 4.00 sec                                               | 3.57 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 825 ms: 2.24x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 892 ms: 2.17x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 479 ms: 2.04x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 367 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 671 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 675 ms: 1.60x faster                                                   |
| async_generators           | 589 ms                                                 | 541 ms: 1.09x faster                                                   |
| coroutines                 | 29.5 ms                                                | 28.4 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.63x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 113 ms: 1.09x faster                                                   |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 157 ms: 1.19x faster                                                   |
| regex_effbot   | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| regex_dna      | 278 ms                                                 | 297 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 143 ms: 1.19x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 205 ms: 1.18x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.59 sec: 1.11x faster                                                 |
| json_loads           | 37.9 us                                                | 34.4 us: 1.10x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 117 ms: 1.09x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 284 us: 1.06x faster                                                   |
| json_dumps           | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.2 ms: 1.16x faster                                                  |
| python_startup         | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                | 63.1 ms: 1.07x faster                                                  |
| mako           | 15.7 ms                                                | 16.9 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 825 ms: 2.24x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 892 ms: 2.17x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 479 ms: 2.04x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 367 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 671 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 675 ms: 1.60x faster                                                   |
| deepcopy                   | 468 us                                                 | 345 us: 1.35x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.7 us: 1.35x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.1 us: 1.28x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.72 ms: 1.28x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 172 ms: 1.27x faster                                                   |
| raytrace                   | 408 ms                                                 | 341 ms: 1.19x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 143 ms: 1.19x faster                                                   |
| pylint                     | 465 ms                                                 | 392 ms: 1.19x faster                                                   |
| regex_compile              | 187 ms                                                 | 157 ms: 1.19x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.60 sec: 1.18x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 205 ms: 1.18x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.53 sec: 1.17x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.09 us: 1.17x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 15.2 ms: 1.16x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 136 ms: 1.15x faster                                                   |
| pathlib                    | 31.6 ms                                                | 27.5 ms: 1.15x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 194 ms: 1.15x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 26.1 ms: 1.14x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.50 sec: 1.13x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 94.6 ms: 1.13x faster                                                  |
| spectral_norm              | 156 ms                                                 | 139 ms: 1.12x faster                                                   |
| nqueens                    | 117 ms                                                 | 104 ms: 1.12x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.57 sec: 1.12x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.59 sec: 1.11x faster                                                 |
| sympy_str                  | 385 ms                                                 | 349 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 87.4 ms: 1.10x faster                                                  |
| logging_format             | 9.59 us                                                | 8.70 us: 1.10x faster                                                  |
| json_loads                 | 37.9 us                                                | 34.4 us: 1.10x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 204 us: 1.10x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.13 ms: 1.09x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.70 us: 1.09x faster                                                  |
| float                      | 123 ms                                                 | 113 ms: 1.09x faster                                                   |
| async_generators           | 589 ms                                                 | 541 ms: 1.09x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 117 ms: 1.09x faster                                                   |
| meteor_contest             | 146 ms                                                 | 135 ms: 1.08x faster                                                   |
| go                         | 172 ms                                                 | 160 ms: 1.08x faster                                                   |
| genshi_xml                 | 67.6 ms                                                | 63.1 ms: 1.07x faster                                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.67 ms: 1.07x faster                                                  |
| scimark_fft                | 500 ms                                                 | 469 ms: 1.07x faster                                                   |
| pyflate                    | 727 ms                                                 | 684 ms: 1.06x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 23.3 ms: 1.06x faster                                                  |
| fannkuch                   | 540 ms                                                 | 510 ms: 1.06x faster                                                   |
| chaos                      | 84.9 ms                                                | 80.2 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 284 us: 1.06x faster                                                   |
| 2to3                       | 456 ms                                                 | 433 ms: 1.05x faster                                                   |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| html5lib                   | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.69 us: 1.05x faster                                                  |
| json                       | 6.85 ms                                                | 6.53 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.89 sec: 1.04x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 928 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 28.4 ms: 1.04x faster                                                  |
| richards                   | 60.3 ms                                                | 63.7 ms: 1.05x slower                                                  |
| regex_dna                  | 278 ms                                                 | 297 ms: 1.07x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| mako                       | 15.7 ms                                                | 16.9 ms: 1.07x slower                                                  |
| python_startup             | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                  |
| telco                      | 9.59 ms                                                | 10.6 ms: 1.10x slower                                                  |
| coverage                   | 95.4 ms                                                | 110 ms: 1.15x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.78 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.17 ms: 1.64x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 84.3 ms: 4.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (19): sqlglot_optimize, thrift, scimark_sparse_mat_mult, asyncio_websockets, dulwich_log, generators, pickle_pure_python, scimark_lu, sympy_expand, xml_etree_process, hexiom, scimark_sor, genshi_text, regex_v8, deltablue, nbody, logging_silent, richards_super, django_template
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x