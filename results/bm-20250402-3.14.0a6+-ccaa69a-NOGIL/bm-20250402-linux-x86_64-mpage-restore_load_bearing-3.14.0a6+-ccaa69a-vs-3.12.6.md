# Results vs. 3.12.6

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.007x faster
- HPT reliability: 96.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 516 ms: 1.13x slower                                                  |
| docutils       | 4.00 sec                                               | 4.30 sec: 1.08x slower                                                |
| html5lib       | 88.9 ms                                                | 103 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 746 ms: 2.59x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 776 ms: 2.38x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 320 ms: 2.20x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.02x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 513 ms: 1.90x faster                                                  |
| async_tree_none            | 741 ms                                                 | 404 ms: 1.83x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 643 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 688 ms: 1.57x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 720 ms: 1.04x faster                                                  |
| coroutines                 | 29.5 ms                                                | 32.5 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.65x faster                                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 89.0 ms: 1.38x faster                                                 |
| pidigits       | 250 ms                                                 | 273 ms: 1.09x slower                                                  |
| nbody          | 119 ms                                                 | 158 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.19 ms: 1.23x faster                                                 |
| regex_v8       | 32.5 ms                                                | 29.6 ms: 1.10x faster                                                 |
| regex_compile  | 187 ms                                                 | 222 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 139 ms: 1.22x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 210 ms: 1.15x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 322 us: 1.07x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 483 us: 1.11x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 94.4 ms: 1.13x slower                                                 |
| json_loads           | 37.9 us                                                | 45.4 us: 1.20x slower                                                 |
| json_dumps           | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 23.7 ms                                                | 33.4 ms: 1.41x slower                                                 |
| python_startup_no_site | 17.6 ms                                                | 24.8 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 34.6 ms: 1.14x slower                                                 |
| genshi_xml      | 67.6 ms                                                | 84.5 ms: 1.25x slower                                                 |
| django_template | 44.9 ms                                                | 59.6 ms: 1.33x slower                                                 |
| mako            | 15.7 ms                                                | 23.4 ms: 1.49x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 746 ms: 2.59x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 776 ms: 2.38x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 320 ms: 2.20x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.02x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 513 ms: 1.90x faster                                                  |
| async_tree_none            | 741 ms                                                 | 404 ms: 1.83x faster                                                  |
| mdp                        | 3.97 sec                                               | 2.31 sec: 1.72x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 643 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 688 ms: 1.57x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.07 ms: 1.44x faster                                                 |
| float                      | 123 ms                                                 | 89.0 ms: 1.38x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.19 ms: 1.23x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 139 ms: 1.22x faster                                                  |
| deepcopy                   | 468 us                                                 | 401 us: 1.17x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 210 ms: 1.15x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 46.8 us: 1.12x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.63 sec: 1.10x faster                                                |
| regex_v8                   | 32.5 ms                                                | 29.6 ms: 1.10x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.56 us: 1.09x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 720 ms: 1.04x faster                                                  |
| raytrace                   | 408 ms                                                 | 425 ms: 1.04x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 233 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 322 us: 1.07x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.30 sec: 1.08x slower                                                |
| pprint_safe_repr           | 967 ms                                                 | 1.04 sec: 1.08x slower                                                |
| richards_super             | 72.8 ms                                                | 78.7 ms: 1.08x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 117 ms: 1.09x slower                                                  |
| pidigits                   | 250 ms                                                 | 273 ms: 1.09x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.43 us: 1.10x slower                                                 |
| richards                   | 60.3 ms                                                | 66.3 ms: 1.10x slower                                                 |
| coroutines                 | 29.5 ms                                                | 32.5 ms: 1.10x slower                                                 |
| go                         | 172 ms                                                 | 190 ms: 1.11x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 483 us: 1.11x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.21 sec: 1.11x slower                                                |
| logging_format             | 9.59 us                                                | 10.7 us: 1.12x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 108 ms: 1.12x slower                                                  |
| sympy_str                  | 385 ms                                                 | 433 ms: 1.12x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 94.4 ms: 1.13x slower                                                 |
| 2to3                       | 456 ms                                                 | 516 ms: 1.13x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 253 ms: 1.14x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.65 ms: 1.14x slower                                                 |
| genshi_text                | 30.2 ms                                                | 34.6 ms: 1.14x slower                                                 |
| meteor_contest             | 146 ms                                                 | 168 ms: 1.15x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.53 ms: 1.15x slower                                                 |
| html5lib                   | 88.9 ms                                                | 103 ms: 1.15x slower                                                  |
| generators                 | 41.1 ms                                                | 47.7 ms: 1.16x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 34.5 ms: 1.16x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.69 sec: 1.17x slower                                                |
| fannkuch                   | 540 ms                                                 | 634 ms: 1.17x slower                                                  |
| json                       | 6.85 ms                                                | 8.12 ms: 1.19x slower                                                 |
| regex_compile              | 187 ms                                                 | 222 ms: 1.19x slower                                                  |
| chaos                      | 84.9 ms                                                | 101 ms: 1.19x slower                                                  |
| json_loads                 | 37.9 us                                                | 45.4 us: 1.20x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 183 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 270 us: 1.20x slower                                                  |
| sympy_expand               | 582 ms                                                 | 709 ms: 1.22x slower                                                  |
| telco                      | 9.59 ms                                                | 11.8 ms: 1.23x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 84.5 ms: 1.25x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 30.9 ms: 1.25x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                 |
| django_template            | 44.9 ms                                                | 59.6 ms: 1.33x slower                                                 |
| nbody                      | 119 ms                                                 | 158 ms: 1.33x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.81 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.70 ms: 1.40x slower                                                 |
| python_startup             | 23.7 ms                                                | 33.4 ms: 1.41x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 24.8 ms: 1.41x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 5.16 ms: 1.48x slower                                                 |
| mako                       | 15.7 ms                                                | 23.4 ms: 1.49x slower                                                 |
| coverage                   | 95.4 ms                                                | 164 ms: 1.72x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 98.5 ms: 4.76x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (15): pathlib, spectral_norm, pyflate, async_generators, dulwich_log, xml_etree_generate, pylint, scimark_fft, tomli_loads, logging_silent, comprehensions, scimark_sor, regex_dna, nqueens, logging_simple
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 96.80% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x