# Results vs. 3.12.6

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.68 sec: 1.08x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 465 ms: 2.10x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 901 ms: 2.05x faster                                                  |
| async_tree_none            | 741 ms                                                 | 379 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 508 ms: 1.83x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 691 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                  |
| async_generators           | 589 ms                                                 | 519 ms: 1.13x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                  |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 96.4 ms: 1.28x faster                                                 |
| Geometric mean | (ref)                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.13 ms: 1.24x faster                                                 |
| regex_compile  | 187 ms                                                 | 171 ms: 1.09x faster                                                  |
| regex_v8       | 32.5 ms                                                | 30.2 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 205 ms: 1.18x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.58 sec: 1.12x faster                                                |
| xml_etree_iterparse | 169 ms                                                 | 158 ms: 1.07x faster                                                  |
| json_loads          | 37.9 us                                                | 41.1 us: 1.08x slower                                                 |
| json_dumps          | 14.3 ms                                                | 15.7 ms: 1.10x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (4): xml_etree_generate, xml_etree_process, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 32.6 ms: 1.37x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                 |
| genshi_xml     | 67.6 ms                                                | 64.4 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                  |
| mdp                        | 3.97 sec                                               | 1.87 sec: 2.13x faster                                                |
| async_tree_memoization     | 977 ms                                                 | 465 ms: 2.10x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 901 ms: 2.05x faster                                                  |
| async_tree_none            | 741 ms                                                 | 379 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 508 ms: 1.83x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 691 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 37.7 us: 1.39x faster                                                 |
| deepcopy                   | 468 us                                                 | 337 us: 1.39x faster                                                  |
| float                      | 123 ms                                                 | 96.4 ms: 1.28x faster                                                 |
| comprehensions             | 27.1 us                                                | 21.3 us: 1.27x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.13 ms: 1.24x faster                                                 |
| raytrace                   | 408 ms                                                 | 334 ms: 1.22x faster                                                  |
| dulwich_log                | 100 ms                                                 | 82.9 ms: 1.21x faster                                                 |
| pyflate                    | 727 ms                                                 | 606 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.43 us: 1.18x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 205 ms: 1.18x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 186 ms: 1.17x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.09 us: 1.17x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 93.8 ms: 1.14x faster                                                 |
| go                         | 172 ms                                                 | 151 ms: 1.14x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 85.0 ms: 1.13x faster                                                 |
| async_generators           | 589 ms                                                 | 519 ms: 1.13x faster                                                  |
| pylint                     | 465 ms                                                 | 412 ms: 1.13x faster                                                  |
| scimark_fft                | 500 ms                                                 | 444 ms: 1.13x faster                                                  |
| spectral_norm              | 156 ms                                                 | 138 ms: 1.13x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.58 sec: 1.12x faster                                                |
| pycparser                  | 1.79 sec                                               | 1.62 sec: 1.11x faster                                                |
| bpe_tokeniser              | 6.59 sec                                               | 5.96 sec: 1.11x faster                                                |
| scimark_sor                | 167 ms                                                 | 151 ms: 1.10x faster                                                  |
| nqueens                    | 117 ms                                                 | 106 ms: 1.10x faster                                                  |
| regex_compile              | 187 ms                                                 | 171 ms: 1.09x faster                                                  |
| chaos                      | 84.9 ms                                                | 77.9 ms: 1.09x faster                                                 |
| pathlib                    | 31.6 ms                                                | 29.1 ms: 1.09x faster                                                 |
| logging_silent             | 139 ns                                                 | 128 ns: 1.09x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.68 sec: 1.08x faster                                                |
| sympy_sum                  | 222 ms                                                 | 205 ms: 1.08x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 30.2 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 158 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 209 us: 1.07x faster                                                  |
| sympy_str                  | 385 ms                                                 | 361 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.30 ms: 1.06x faster                                                 |
| genshi_text                | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                 |
| genshi_xml                 | 67.6 ms                                                | 64.4 ms: 1.05x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.70 us: 1.05x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                  |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                 |
| sympy_expand               | 582 ms                                                 | 620 ms: 1.07x slower                                                  |
| json_loads                 | 37.9 us                                                | 41.1 us: 1.08x slower                                                 |
| telco                      | 9.59 ms                                                | 10.4 ms: 1.09x slower                                                 |
| deltablue                  | 4.27 ms                                                | 4.65 ms: 1.09x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 15.7 ms: 1.10x slower                                                 |
| coverage                   | 95.4 ms                                                | 111 ms: 1.16x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.6 ms: 1.37x slower                                                 |
| gc_traversal               | 5.86 ms                                                | 8.14 ms: 1.39x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 3.69 ms: 1.90x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 95.9 ms: 4.64x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (25): xml_etree_generate, sympy_integrate, nbody, richards_super, xml_etree_process, unpickle_pure_python, richards, fannkuch, pidigits, mako, meteor_contest, logging_format, pickle_pure_python, pprint_safe_repr, pprint_pformat, python_startup_no_site, json, hexiom, regex_dna, django_template, scimark_lu, generators, sqlalchemy_imperative, 2to3, bench_thread_pool
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250402-3.14.0a6+-ccaa69a/bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x