# Results vs. 3.12.6

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.03x faster
- HPT reliability: 91.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 4.14 sec: 1.04x slower                                                |
| html5lib       | 88.9 ms                                                | 94.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.30 sec: 1.49x faster                                                |
| async_tree_none            | 741 ms                                                 | 501 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 485 ms: 1.45x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.44x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 650 ms: 1.43x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 705 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 829 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 856 ms: 1.26x faster                                                  |
| coroutines                 | 29.5 ms                                                | 32.6 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmark hidden because not significant (4): async_generators, asyncio_tcp_ssl, asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 5.47 ms: 1.07x slower                                                 |
| regex_dna      | 278 ms                                                 | 300 ms: 1.08x slower                                                  |
| regex_v8       | 32.5 ms                                                | 38.1 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict     | 52.7 us                                                | 46.2 us: 1.14x faster                                                 |
| tomli_loads     | 2.88 sec                                               | 2.66 sec: 1.08x faster                                                |
| xml_etree_parse | 241 ms                                                 | 226 ms: 1.06x faster                                                  |
| pickle          | 16.4 us                                                | 15.4 us: 1.06x faster                                                 |
| pickle_list     | 6.97 us                                                | 6.74 us: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (9): xml_etree_generate, unpickle_pure_python, xml_etree_iterparse, json_loads, unpickle_list, pickle_pure_python, json_dumps, unpickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 72.0 ms: 1.07x slower                                                 |
| django_template | 44.9 ms                                                | 48.3 ms: 1.08x slower                                                 |
| mako            | 15.7 ms                                                | 18.3 ms: 1.16x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.30 sec: 1.49x faster                                                |
| async_tree_none            | 741 ms                                                 | 501 ms: 1.48x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 485 ms: 1.45x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.44x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 650 ms: 1.43x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 705 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 829 ms: 1.33x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 40.2 us: 1.30x faster                                                 |
| deepcopy                   | 468 us                                                 | 359 us: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 856 ms: 1.26x faster                                                  |
| raytrace                   | 408 ms                                                 | 340 ms: 1.20x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                 |
| pickle_dict                | 52.7 us                                                | 46.2 us: 1.14x faster                                                 |
| comprehensions             | 27.1 us                                                | 24.0 us: 1.13x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.46 us: 1.12x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.63 us: 1.11x faster                                                 |
| nqueens                    | 117 ms                                                 | 105 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.08 sec: 1.08x faster                                                |
| tomli_loads                | 2.88 sec                                               | 2.66 sec: 1.08x faster                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 89.4 ms: 1.08x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 146 ms: 1.07x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.67 sec: 1.07x faster                                                |
| mdp                        | 3.97 sec                                               | 3.71 sec: 1.07x faster                                                |
| pyflate                    | 727 ms                                                 | 682 ms: 1.07x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 226 ms: 1.06x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.7 ms: 1.06x faster                                                 |
| pickle                     | 16.4 us                                                | 15.4 us: 1.06x faster                                                 |
| sympy_integrate            | 29.8 ms                                                | 28.1 ms: 1.06x faster                                                 |
| scimark_fft                | 500 ms                                                 | 476 ms: 1.05x faster                                                  |
| meteor_contest             | 146 ms                                                 | 139 ms: 1.05x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 5.59 ms: 1.05x faster                                                 |
| pickle_list                | 6.97 us                                                | 6.74 us: 1.03x faster                                                 |
| docutils                   | 4.00 sec                                               | 4.14 sec: 1.04x slower                                                |
| sympy_expand               | 582 ms                                                 | 606 ms: 1.04x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.89 ms: 1.06x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.10 us: 1.06x slower                                                 |
| html5lib                   | 88.9 ms                                                | 94.3 ms: 1.06x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 72.0 ms: 1.07x slower                                                 |
| logging_format             | 9.59 us                                                | 10.2 us: 1.07x slower                                                 |
| regex_effbot               | 5.13 ms                                                | 5.47 ms: 1.07x slower                                                 |
| django_template            | 44.9 ms                                                | 48.3 ms: 1.08x slower                                                 |
| regex_dna                  | 278 ms                                                 | 300 ms: 1.08x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.15 ms: 1.08x slower                                                 |
| coroutines                 | 29.5 ms                                                | 32.6 ms: 1.10x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 83.9 ms: 1.10x slower                                                 |
| richards                   | 60.3 ms                                                | 69.2 ms: 1.15x slower                                                 |
| go                         | 172 ms                                                 | 198 ms: 1.15x slower                                                  |
| mako                       | 15.7 ms                                                | 18.3 ms: 1.16x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 38.1 ms: 1.17x slower                                                 |
| telco                      | 9.59 ms                                                | 11.5 ms: 1.20x slower                                                 |
| coverage                   | 95.4 ms                                                | 117 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.41 ms: 1.24x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (44): sympy_str, float, xml_etree_generate, typing_runtime_protocols, crypto_pyaes, tornado_http, 2to3, pprint_pformat, pidigits, async_generators, scimark_sparse_mat_mult, unpickle_pure_python, json, fannkuch, bench_thread_pool, xml_etree_iterparse, asyncio_tcp_ssl, json_loads, logging_silent, unpickle_list, pickle_pure_python, python_startup, generators, spectral_norm, nbody, json_dumps, sqlglot_transpile, asyncio_tcp, unpack_sequence, sympy_sum, unpickle, scimark_sor, asyncio_websockets, pylint, pprint_safe_repr, regex_compile, hexiom, bench_mp_pool, scimark_lu, xml_etree_process, deltablue, chaos, richards_super, genshi_text
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 91.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x