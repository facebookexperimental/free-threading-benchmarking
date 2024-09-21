# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 410 ms: 1.11x faster                                  |
| tornado_http   | 266 ms                                                 | 247 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                          |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 584 ms: 1.59x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.24 sec: 1.56x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 464 ms: 1.52x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 671 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.44x faster                                |
| async_tree_none            | 741 ms                                                 | 531 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 818 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 821 ms: 1.31x faster                                  |
| async_generators           | 589 ms                                                 | 570 ms: 1.03x faster                                  |
| Geometric mean             | (ref)                                                  | 1.25x faster                                          |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, asyncio_websockets, coroutines, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                  |
| nbody          | 119 ms                                                 | 114 ms: 1.04x faster                                  |
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.86 ms: 1.06x faster                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|--------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict        | 52.7 us                                                | 45.4 us: 1.16x faster                                 |
| xml_etree_parse    | 241 ms                                                 | 216 ms: 1.12x faster                                  |
| pickle_list        | 6.97 us                                                | 6.29 us: 1.11x faster                                 |
| xml_etree_generate | 127 ms                                                 | 116 ms: 1.10x faster                                  |
| tomli_loads        | 2.88 sec                                               | 2.68 sec: 1.08x faster                                |
| unpickle           | 21.2 us                                                | 20.1 us: 1.06x faster                                 |
| Geometric mean     | (ref)                                                  | 1.05x faster                                          |

Benchmark hidden because not significant (8): xml_etree_iterparse, pickle_pure_python, pickle, unpickle_pure_python, unpickle_list, xml_etree_process, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.8 ms: 1.19x faster                                 |
| python_startup         | 23.7 ms                                                | 21.4 ms: 1.11x faster                                 |
| Geometric mean         | (ref)                                                  | 1.15x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| mako           | 15.7 ms                                                | 16.5 ms: 1.05x slower                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmark hidden because not significant (3): django_template, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 584 ms: 1.59x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.24 sec: 1.56x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 464 ms: 1.52x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 671 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.44x faster                                |
| async_tree_none            | 741 ms                                                 | 531 ms: 1.40x faster                                  |
| deepcopy_memo              | 52.4 us                                                | 38.7 us: 1.35x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 818 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 821 ms: 1.31x faster                                  |
| deepcopy                   | 468 us                                                 | 361 us: 1.29x faster                                  |
| comprehensions             | 27.1 us                                                | 21.3 us: 1.28x faster                                 |
| raytrace                   | 408 ms                                                 | 339 ms: 1.20x faster                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.8 ms: 1.19x faster                                 |
| pickle_dict                | 52.7 us                                                | 45.4 us: 1.16x faster                                 |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                |
| logging_simple             | 9.45 us                                                | 8.31 us: 1.14x faster                                 |
| xml_etree_parse            | 241 ms                                                 | 216 ms: 1.12x faster                                  |
| 2to3                       | 456 ms                                                 | 410 ms: 1.11x faster                                  |
| pickle_list                | 6.97 us                                                | 6.29 us: 1.11x faster                                 |
| python_startup             | 23.7 ms                                                | 21.4 ms: 1.11x faster                                 |
| pathlib                    | 31.6 ms                                                | 28.6 ms: 1.11x faster                                 |
| logging_silent             | 139 ns                                                 | 126 ns: 1.10x faster                                  |
| mdp                        | 3.97 sec                                               | 3.61 sec: 1.10x faster                                |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.13 ms: 1.10x faster                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 88.4 ms: 1.09x faster                                 |
| nqueens                    | 117 ms                                                 | 107 ms: 1.09x faster                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.71 us: 1.09x faster                                 |
| pyflate                    | 727 ms                                                 | 669 ms: 1.09x faster                                  |
| tomli_loads                | 2.88 sec                                               | 2.68 sec: 1.08x faster                                |
| tornado_http               | 266 ms                                                 | 247 ms: 1.08x faster                                  |
| generators                 | 41.1 ms                                                | 38.3 ms: 1.07x faster                                 |
| sympy_str                  | 385 ms                                                 | 360 ms: 1.07x faster                                  |
| typing_runtime_protocols   | 224 us                                                 | 210 us: 1.07x faster                                  |
| float                      | 123 ms                                                 | 115 ms: 1.07x faster                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.17 sec: 1.07x faster                                |
| richards_super             | 72.8 ms                                                | 68.7 ms: 1.06x faster                                 |
| unpickle                   | 21.2 us                                                | 20.1 us: 1.06x faster                                 |
| crypto_pyaes               | 107 ms                                                 | 102 ms: 1.06x faster                                  |
| regex_effbot               | 5.13 ms                                                | 4.86 ms: 1.06x faster                                 |
| scimark_fft                | 500 ms                                                 | 478 ms: 1.05x faster                                  |
| sqlite_synth               | 3.87 us                                                | 3.71 us: 1.05x faster                                 |
| nbody                      | 119 ms                                                 | 114 ms: 1.04x faster                                  |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                  |
| chaos                      | 84.9 ms                                                | 81.6 ms: 1.04x faster                                 |
| async_generators           | 589 ms                                                 | 570 ms: 1.03x faster                                  |
| pprint_pformat             | 1.98 sec                                               | 1.92 sec: 1.03x faster                                |
| sympy_expand               | 582 ms                                                 | 605 ms: 1.04x slower                                  |
| mako                       | 15.7 ms                                                | 16.5 ms: 1.05x slower                                 |
| spectral_norm              | 156 ms                                                 | 164 ms: 1.05x slower                                  |
| go                         | 172 ms                                                 | 191 ms: 1.11x slower                                  |
| json                       | 6.85 ms                                                | 7.74 ms: 1.13x slower                                 |
| telco                      | 9.59 ms                                                | 11.1 ms: 1.16x slower                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.27 ms: 1.17x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 78.4 ns: 1.30x slower                                 |
| coverage                   | 95.4 ms                                                | 126 ms: 1.32x slower                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                          |

Benchmark hidden because not significant (42): xml_etree_iterparse, sqlglot_normalize, dulwich_log, pickle_pure_python, sympy_sum, sqlglot_parse, sqlglot_optimize, gc_traversal, pickle, thrift, regex_compile, logging_format, bench_mp_pool, bench_thread_pool, sympy_integrate, unpickle_pure_python, docutils, pprint_safe_repr, scimark_sparse_mat_mult, unpickle_list, fannkuch, dask, html5lib, meteor_contest, richards, xml_etree_process, json_loads, hexiom, asyncio_tcp_ssl, asyncio_websockets, django_template, deltablue, regex_v8, scimark_lu, coroutines, pylint, regex_dna, genshi_xml, genshi_text, json_dumps, asyncio_tcp, scimark_sor
Ignored benchmarks (7) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x