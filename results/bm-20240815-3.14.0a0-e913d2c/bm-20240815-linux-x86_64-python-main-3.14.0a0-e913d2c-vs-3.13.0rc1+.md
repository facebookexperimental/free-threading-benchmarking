# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.01x faster
- HPT reliability: 95.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 422 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                   | 1.03x faster                                          |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg       | 1.46 sec                                                | 1.27 sec: 1.14x faster                                |
| async_tree_none        | 576 ms                                                  | 508 ms: 1.13x faster                                  |
| async_tree_none_tg     | 521 ms                                                  | 466 ms: 1.12x faster                                  |
| async_tree_memoization | 745 ms                                                  | 670 ms: 1.11x faster                                  |
| async_tree_io          | 1.38 sec                                                | 1.29 sec: 1.07x faster                                |
| asyncio_websockets     | 772 ms                                                  | 734 ms: 1.05x faster                                  |
| async_generators       | 592 ms                                                  | 574 ms: 1.03x faster                                  |
| coroutines             | 29.2 ms                                                 | 31.3 ms: 1.07x slower                                 |
| Geometric mean         | (ref)                                                   | 1.05x faster                                          |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_memoization_tg, asyncio_tcp, async_tree_cpu_io_mixed_tg, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 124 ms                                                  | 116 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                   | 1.00x slower                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 35.4 ms: 1.09x slower                                 |
| regex_effbot   | 4.84 ms                                                 | 5.30 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                   | 1.05x slower                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_pure_python | 296 us                                                  | 275 us: 1.08x faster                                  |
| xml_etree_generate   | 129 ms                                                  | 121 ms: 1.07x faster                                  |
| unpickle             | 21.4 us                                                 | 20.4 us: 1.05x faster                                 |
| tomli_loads          | 2.80 sec                                                | 2.73 sec: 1.03x faster                                |
| json_loads           | 36.1 us                                                 | 37.6 us: 1.04x slower                                 |
| json_dumps           | 14.9 ms                                                 | 15.7 ms: 1.06x slower                                 |
| unpickle_list        | 6.67 us                                                 | 7.68 us: 1.15x slower                                 |
| Geometric mean       | (ref)                                                   | 1.00x slower                                          |

Benchmark hidden because not significant (7): xml_etree_iterparse, xml_etree_parse, pickle_list, xml_etree_process, pickle, pickle_dict, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 15.4 ms: 1.05x slower                                 |
| Geometric mean         | (ref)                                                   | 1.04x slower                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml     | 68.3 ms                                                 | 71.8 ms: 1.05x slower                                 |
| mako           | 16.1 ms                                                 | 17.0 ms: 1.06x slower                                 |
| Geometric mean | (ref)                                                   | 1.03x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy_memo            | 51.7 us                                                 | 39.8 us: 1.30x faster                                 |
| deepcopy                 | 484 us                                                  | 383 us: 1.26x faster                                  |
| async_tree_io_tg         | 1.46 sec                                                | 1.27 sec: 1.14x faster                                |
| async_tree_none          | 576 ms                                                  | 508 ms: 1.13x faster                                  |
| async_tree_none_tg       | 521 ms                                                  | 466 ms: 1.12x faster                                  |
| deepcopy_reduce          | 4.27 us                                                 | 3.83 us: 1.12x faster                                 |
| async_tree_memoization   | 745 ms                                                  | 670 ms: 1.11x faster                                  |
| unpack_sequence          | 73.9 ns                                                 | 66.6 ns: 1.11x faster                                 |
| sympy_integrate          | 29.7 ms                                                 | 27.3 ms: 1.09x faster                                 |
| logging_simple           | 8.98 us                                                 | 8.33 us: 1.08x faster                                 |
| unpickle_pure_python     | 296 us                                                  | 275 us: 1.08x faster                                  |
| async_tree_io            | 1.38 sec                                                | 1.29 sec: 1.07x faster                                |
| richards_super           | 76.3 ms                                                 | 71.2 ms: 1.07x faster                                 |
| sqlite_synth             | 4.07 us                                                 | 3.80 us: 1.07x faster                                 |
| xml_etree_generate       | 129 ms                                                  | 121 ms: 1.07x faster                                  |
| raytrace                 | 350 ms                                                  | 328 ms: 1.07x faster                                  |
| nbody                    | 124 ms                                                  | 116 ms: 1.07x faster                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 71.7 ms: 1.06x faster                                 |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 6.60 ms: 1.06x faster                                 |
| asyncio_websockets       | 772 ms                                                  | 734 ms: 1.05x faster                                  |
| pathlib                  | 29.3 ms                                                 | 28.0 ms: 1.05x faster                                 |
| 2to3                     | 442 ms                                                  | 422 ms: 1.05x faster                                  |
| meteor_contest           | 157 ms                                                  | 150 ms: 1.05x faster                                  |
| unpickle                 | 21.4 us                                                 | 20.4 us: 1.05x faster                                 |
| async_generators         | 592 ms                                                  | 574 ms: 1.03x faster                                  |
| tomli_loads              | 2.80 sec                                                | 2.73 sec: 1.03x faster                                |
| json_loads               | 36.1 us                                                 | 37.6 us: 1.04x slower                                 |
| generators               | 39.2 ms                                                 | 41.0 ms: 1.05x slower                                 |
| genshi_xml               | 68.3 ms                                                 | 71.8 ms: 1.05x slower                                 |
| python_startup_no_site   | 14.6 ms                                                 | 15.4 ms: 1.05x slower                                 |
| json_dumps               | 14.9 ms                                                 | 15.7 ms: 1.06x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 106 ms: 1.06x slower                                  |
| mako                     | 16.1 ms                                                 | 17.0 ms: 1.06x slower                                 |
| coverage                 | 110 ms                                                  | 117 ms: 1.06x slower                                  |
| pycparser                | 1.57 sec                                                | 1.67 sec: 1.06x slower                                |
| comprehensions           | 20.9 us                                                 | 22.4 us: 1.07x slower                                 |
| thrift                   | 1.11 ms                                                 | 1.19 ms: 1.07x slower                                 |
| coroutines               | 29.2 ms                                                 | 31.3 ms: 1.07x slower                                 |
| scimark_fft              | 477 ms                                                  | 510 ms: 1.07x slower                                  |
| nqueens                  | 108 ms                                                  | 116 ms: 1.07x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 233 us: 1.08x slower                                  |
| sympy_sum                | 213 ms                                                  | 230 ms: 1.08x slower                                  |
| regex_v8                 | 32.4 ms                                                 | 35.4 ms: 1.09x slower                                 |
| regex_effbot             | 4.84 ms                                                 | 5.30 ms: 1.09x slower                                 |
| json                     | 6.55 ms                                                 | 7.54 ms: 1.15x slower                                 |
| unpickle_list            | 6.67 us                                                 | 7.68 us: 1.15x slower                                 |
| bench_thread_pool        | 3.06 ms                                                 | 3.58 ms: 1.17x slower                                 |
| Geometric mean           | (ref)                                                   | 1.01x faster                                          |

Benchmark hidden because not significant (49): xml_etree_iterparse, async_tree_cpu_io_mixed, html5lib, xml_etree_parse, gc_traversal, chaos, richards, async_tree_memoization_tg, deltablue, tornado_http, sqlglot_transpile, spectral_norm, asyncio_tcp, mdp, fannkuch, scimark_sor, telco, pprint_pformat, sympy_expand, scimark_monte_carlo, scimark_lu, regex_compile, pickle_list, async_tree_cpu_io_mixed_tg, pprint_safe_repr, xml_etree_process, go, sqlglot_parse, django_template, logging_format, docutils, sympy_str, bpe_tokeniser, sqlglot_normalize, asyncio_tcp_ssl, regex_dna, pyflate, genshi_text, pylint, create_gc_cycles, hexiom, python_startup, pidigits, pickle, pickle_dict, bench_mp_pool, pickle_pure_python, logging_silent, float
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 95.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x