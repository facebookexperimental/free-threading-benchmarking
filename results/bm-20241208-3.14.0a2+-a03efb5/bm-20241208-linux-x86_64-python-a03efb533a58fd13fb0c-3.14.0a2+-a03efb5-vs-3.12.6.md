# Results vs. 3.12.6

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 411 ms: 1.11x faster                                                   |
| docutils       | 4.00 sec                                               | 3.58 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 82.5 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 855 ms: 2.26x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 839 ms: 2.20x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 481 ms: 2.03x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 479 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 668 ms: 1.61x faster                                                   |
| async_generators           | 589 ms                                                 | 523 ms: 1.13x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 707 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.63x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 112 ms: 1.10x faster                                                   |
| pidigits       | 250 ms                                                 | 230 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| regex_compile  | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 138 ms: 1.23x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| json_loads           | 37.9 us                                                | 33.4 us: 1.13x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 113 ms: 1.12x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 78.3 ms: 1.07x faster                                                  |
| tomli_loads          | 2.88 sec                                               | 2.70 sec: 1.07x faster                                                 |
| unpickle_pure_python | 300 us                                                 | 281 us: 1.07x faster                                                   |
| json_dumps           | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 16.6 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 855 ms: 2.26x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 839 ms: 2.20x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 481 ms: 2.03x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 479 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 668 ms: 1.61x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.2 us: 1.37x faster                                                  |
| deepcopy                   | 468 us                                                 | 344 us: 1.36x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.2 us: 1.28x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.72 ms: 1.28x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 174 ms: 1.25x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.45 sec: 1.23x faster                                                 |
| pylint                     | 465 ms                                                 | 377 ms: 1.23x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 138 ms: 1.23x faster                                                   |
| pathlib                    | 31.6 ms                                                | 25.8 ms: 1.23x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| raytrace                   | 408 ms                                                 | 345 ms: 1.18x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.16 us: 1.16x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 92.9 ms: 1.15x faster                                                  |
| nqueens                    | 117 ms                                                 | 101 ms: 1.15x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 192 ms: 1.15x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.4 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.73 sec: 1.15x faster                                                 |
| go                         | 172 ms                                                 | 151 ms: 1.14x faster                                                   |
| regex_compile              | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| json_loads                 | 37.9 us                                                | 33.4 us: 1.13x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 139 ms: 1.13x faster                                                   |
| async_generators           | 589 ms                                                 | 523 ms: 1.13x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 113 ms: 1.12x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.54 sec: 1.12x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.58 sec: 1.12x faster                                                 |
| fannkuch                   | 540 ms                                                 | 484 ms: 1.12x faster                                                   |
| 2to3                       | 456 ms                                                 | 411 ms: 1.11x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.64 us: 1.11x faster                                                  |
| pyflate                    | 727 ms                                                 | 662 ms: 1.10x faster                                                   |
| float                      | 123 ms                                                 | 112 ms: 1.10x faster                                                   |
| logging_format             | 9.59 us                                                | 8.77 us: 1.09x faster                                                  |
| json                       | 6.85 ms                                                | 6.28 ms: 1.09x faster                                                  |
| richards_super             | 72.8 ms                                                | 66.9 ms: 1.09x faster                                                  |
| pidigits                   | 250 ms                                                 | 230 ms: 1.09x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 27.6 ms: 1.08x faster                                                  |
| html5lib                   | 88.9 ms                                                | 82.5 ms: 1.08x faster                                                  |
| thrift                     | 1.06 ms                                                | 985 us: 1.08x faster                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.66 ms: 1.07x faster                                                  |
| dulwich_log                | 100 ms                                                 | 93.4 ms: 1.07x faster                                                  |
| sympy_str                  | 385 ms                                                 | 359 ms: 1.07x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.18 ms: 1.07x faster                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 71.0 ms: 1.07x faster                                                  |
| generators                 | 41.1 ms                                                | 38.4 ms: 1.07x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 78.3 ms: 1.07x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.70 sec: 1.07x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 281 us: 1.07x faster                                                   |
| scimark_fft                | 500 ms                                                 | 470 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 211 us: 1.06x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 707 ms: 1.06x faster                                                   |
| scimark_sor                | 167 ms                                                 | 158 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.36 ms: 1.05x faster                                                  |
| richards                   | 60.3 ms                                                | 57.7 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 92.2 ms: 1.04x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.71 us: 1.04x faster                                                  |
| chaos                      | 84.9 ms                                                | 81.7 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.92 sec: 1.03x faster                                                 |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| mako                       | 15.7 ms                                                | 16.6 ms: 1.05x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.09x slower                                                  |
| coverage                   | 95.4 ms                                                | 112 ms: 1.17x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.38 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.43 ms: 1.77x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 85.0 ms: 4.11x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (16): genshi_xml, genshi_text, regex_dna, deltablue, pickle_pure_python, sympy_expand, pprint_safe_repr, hexiom, scimark_lu, spectral_norm, logging_silent, regex_v8, django_template, python_startup, nbody, meteor_contest
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x