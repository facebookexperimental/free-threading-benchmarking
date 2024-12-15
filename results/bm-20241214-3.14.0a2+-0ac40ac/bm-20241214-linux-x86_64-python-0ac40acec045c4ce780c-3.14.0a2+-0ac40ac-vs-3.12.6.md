# Results vs. 3.12.6

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.128x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 418 ms: 1.09x faster                                                   |
| docutils       | 4.00 sec                                               | 3.55 sec: 1.13x faster                                                 |
| html5lib       | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 888 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 862 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 444 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 478 ms: 2.05x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 362 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 670 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 677 ms: 1.59x faster                                                   |
| async_generators           | 589 ms                                                 | 543 ms: 1.08x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 109 ms: 1.13x faster                                                   |
| pidigits       | 250 ms                                                 | 241 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                  |
| regex_compile  | 187 ms                                                 | 163 ms: 1.14x faster                                                   |
| regex_dna      | 278 ms                                                 | 269 ms: 1.03x faster                                                   |
| regex_v8       | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 189 ms: 1.28x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.56 sec: 1.13x faster                                                 |
| json_loads          | 37.9 us                                                | 33.9 us: 1.12x faster                                                  |
| xml_etree_generate  | 127 ms                                                 | 115 ms: 1.11x faster                                                   |
| pickle_pure_python  | 436 us                                                 | 403 us: 1.08x faster                                                   |
| xml_etree_process   | 83.7 ms                                                | 80.0 ms: 1.05x faster                                                  |
| json_dumps          | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.3 ms: 1.23x faster                                                  |
| python_startup         | 23.7 ms                                                | 24.4 ms: 1.03x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_text, genshi_xml, mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 888 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 862 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 444 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 478 ms: 2.05x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 362 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 670 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 677 ms: 1.59x faster                                                   |
| deepcopy                   | 468 us                                                 | 336 us: 1.39x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 163 ms: 1.33x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 189 ms: 1.28x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.3 us: 1.27x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.3 ms: 1.23x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 42.7 us: 1.23x faster                                                  |
| pathlib                    | 31.6 ms                                                | 25.7 ms: 1.23x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.48 sec: 1.21x faster                                                 |
| bench_thread_pool          | 3.48 ms                                                | 2.89 ms: 1.21x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.08 us: 1.17x faster                                                  |
| pylint                     | 465 ms                                                 | 398 ms: 1.17x faster                                                   |
| raytrace                   | 408 ms                                                 | 350 ms: 1.16x faster                                                   |
| spectral_norm              | 156 ms                                                 | 134 ms: 1.16x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 92.5 ms: 1.16x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.79 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| sqlglot_normalize          | 157 ms                                                 | 136 ms: 1.15x faster                                                   |
| pyflate                    | 727 ms                                                 | 633 ms: 1.15x faster                                                   |
| regex_compile              | 187 ms                                                 | 163 ms: 1.14x faster                                                   |
| float                      | 123 ms                                                 | 109 ms: 1.13x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.55 sec: 1.13x faster                                                 |
| go                         | 172 ms                                                 | 153 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.85 sec: 1.13x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.56 sec: 1.13x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.09 ms: 1.12x faster                                                  |
| json_loads                 | 37.9 us                                                | 33.9 us: 1.12x faster                                                  |
| nqueens                    | 117 ms                                                 | 106 ms: 1.11x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 115 ms: 1.11x faster                                                   |
| scimark_fft                | 500 ms                                                 | 454 ms: 1.10x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.4 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 87.8 ms: 1.10x faster                                                  |
| 2to3                       | 456 ms                                                 | 418 ms: 1.09x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 69.7 ms: 1.09x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 204 ms: 1.09x faster                                                   |
| async_generators           | 589 ms                                                 | 543 ms: 1.08x faster                                                   |
| logging_format             | 9.59 us                                                | 8.84 us: 1.08x faster                                                  |
| meteor_contest             | 146 ms                                                 | 135 ms: 1.08x faster                                                   |
| richards_super             | 72.8 ms                                                | 67.3 ms: 1.08x faster                                                  |
| pickle_pure_python         | 436 us                                                 | 403 us: 1.08x faster                                                   |
| scimark_sor                | 167 ms                                                 | 154 ms: 1.08x faster                                                   |
| html5lib                   | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| generators                 | 41.1 ms                                                | 38.4 ms: 1.07x faster                                                  |
| json                       | 6.85 ms                                                | 6.40 ms: 1.07x faster                                                  |
| fannkuch                   | 540 ms                                                 | 507 ms: 1.07x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 28.0 ms: 1.06x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.66 us: 1.06x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.82 us: 1.06x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.85 ms: 1.05x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.77 sec: 1.05x faster                                                 |
| chaos                      | 84.9 ms                                                | 80.6 ms: 1.05x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.06 ms: 1.05x faster                                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.71 ms: 1.05x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 80.0 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.89 sec: 1.05x faster                                                 |
| regex_dna                  | 278 ms                                                 | 269 ms: 1.03x faster                                                   |
| pidigits                   | 250 ms                                                 | 241 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 935 ms: 1.03x faster                                                   |
| python_startup             | 23.7 ms                                                | 24.4 ms: 1.03x slower                                                  |
| telco                      | 9.59 ms                                                | 10.0 ms: 1.04x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                  |
| coverage                   | 95.4 ms                                                | 117 ms: 1.23x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.90 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.35 ms: 1.73x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 89.8 ms: 4.34x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (15): dulwich_log, unpickle_pure_python, scimark_lu, genshi_text, genshi_xml, richards, sympy_str, sympy_expand, logging_silent, mako, django_template, nbody, thrift, asyncio_websockets, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.128x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x