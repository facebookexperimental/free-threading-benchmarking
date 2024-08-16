# Results vs. 3.13.0rc1+

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.00x faster
- HPT reliability: 77.09%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                | 4.14 sec: 1.03x slower                                                |
| Geometric mean | (ref)                                                   | 1.01x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|--------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none    | 576 ms                                                  | 501 ms: 1.15x faster                                                  |
| async_tree_io_tg   | 1.46 sec                                                | 1.30 sec: 1.12x faster                                                |
| async_tree_none_tg | 521 ms                                                  | 485 ms: 1.07x faster                                                  |
| async_tree_io      | 1.38 sec                                                | 1.29 sec: 1.07x faster                                                |
| asyncio_tcp        | 985 ms                                                  | 940 ms: 1.05x faster                                                  |
| coroutines         | 29.2 ms                                                 | 32.6 ms: 1.12x slower                                                 |
| Geometric mean     | (ref)                                                   | 1.04x faster                                                          |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_generators, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 300 ms: 1.04x slower                                                  |
| regex_compile  | 177 ms                                                  | 192 ms: 1.08x slower                                                  |
| regex_effbot   | 4.84 ms                                                 | 5.47 ms: 1.13x slower                                                 |
| regex_v8       | 32.4 ms                                                 | 38.1 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                   | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|--------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads        | 2.80 sec                                                | 2.66 sec: 1.05x faster                                                |
| xml_etree_parse    | 236 ms                                                  | 226 ms: 1.04x faster                                                  |
| pickle_pure_python | 417 us                                                  | 436 us: 1.05x slower                                                  |
| Geometric mean     | (ref)                                                   | 1.01x faster                                                          |

Benchmark hidden because not significant (11): xml_etree_iterparse, xml_etree_generate, json_dumps, pickle_list, pickle_dict, unpickle_pure_python, pickle, xml_etree_process, unpickle, unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                 | 23.8 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                   | 1.05x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 16.1 ms                                                 | 18.3 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                   | 1.06x slower                                                          |

Benchmark hidden because not significant (3): genshi_text, django_template, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                | 484 us                                                  | 359 us: 1.35x faster                                                  |
| deepcopy_memo           | 51.7 us                                                 | 40.2 us: 1.29x faster                                                 |
| unpack_sequence         | 73.9 ns                                                 | 61.3 ns: 1.20x faster                                                 |
| deepcopy_reduce         | 4.27 us                                                 | 3.63 us: 1.18x faster                                                 |
| async_tree_none         | 576 ms                                                  | 501 ms: 1.15x faster                                                  |
| meteor_contest          | 157 ms                                                  | 139 ms: 1.13x faster                                                  |
| async_tree_io_tg        | 1.46 sec                                                | 1.30 sec: 1.12x faster                                                |
| async_tree_none_tg      | 521 ms                                                  | 485 ms: 1.07x faster                                                  |
| async_tree_io           | 1.38 sec                                                | 1.29 sec: 1.07x faster                                                |
| logging_simple          | 8.98 us                                                 | 8.46 us: 1.06x faster                                                 |
| scimark_sparse_mat_mult | 6.98 ms                                                 | 6.59 ms: 1.06x faster                                                 |
| gc_traversal            | 5.91 ms                                                 | 5.59 ms: 1.06x faster                                                 |
| sympy_integrate         | 29.7 ms                                                 | 28.1 ms: 1.06x faster                                                 |
| tomli_loads             | 2.80 sec                                                | 2.66 sec: 1.05x faster                                                |
| asyncio_tcp             | 985 ms                                                  | 940 ms: 1.05x faster                                                  |
| xml_etree_parse         | 236 ms                                                  | 226 ms: 1.04x faster                                                  |
| sympy_expand            | 631 ms                                                  | 606 ms: 1.04x faster                                                  |
| pprint_pformat          | 2.00 sec                                                | 1.94 sec: 1.03x faster                                                |
| bpe_tokeniser           | 6.25 sec                                                | 6.08 sec: 1.03x faster                                                |
| docutils                | 4.01 sec                                                | 4.14 sec: 1.03x slower                                                |
| pprint_safe_repr        | 959 ms                                                  | 995 ms: 1.04x slower                                                  |
| regex_dna               | 288 ms                                                  | 300 ms: 1.04x slower                                                  |
| crypto_pyaes            | 99.8 ms                                                 | 105 ms: 1.05x slower                                                  |
| pickle_pure_python      | 417 us                                                  | 436 us: 1.05x slower                                                  |
| generators              | 39.2 ms                                                 | 41.5 ms: 1.06x slower                                                 |
| sympy_sum               | 213 ms                                                  | 226 ms: 1.06x slower                                                  |
| pycparser               | 1.57 sec                                                | 1.67 sec: 1.06x slower                                                |
| coverage                | 110 ms                                                  | 117 ms: 1.07x slower                                                  |
| logging_silent          | 130 ns                                                  | 139 ns: 1.07x slower                                                  |
| logging_format          | 9.48 us                                                 | 10.2 us: 1.08x slower                                                 |
| python_startup          | 22.0 ms                                                 | 23.8 ms: 1.08x slower                                                 |
| regex_compile           | 177 ms                                                  | 192 ms: 1.08x slower                                                  |
| sqlglot_optimize        | 76.2 ms                                                 | 83.9 ms: 1.10x slower                                                 |
| bench_mp_pool           | 19.4 ms                                                 | 21.4 ms: 1.10x slower                                                 |
| coroutines              | 29.2 ms                                                 | 32.6 ms: 1.12x slower                                                 |
| bench_thread_pool       | 3.06 ms                                                 | 3.44 ms: 1.12x slower                                                 |
| regex_effbot            | 4.84 ms                                                 | 5.47 ms: 1.13x slower                                                 |
| mako                    | 16.1 ms                                                 | 18.3 ms: 1.14x slower                                                 |
| comprehensions          | 20.9 us                                                 | 24.0 us: 1.14x slower                                                 |
| regex_v8                | 32.4 ms                                                 | 38.1 ms: 1.17x slower                                                 |
| Geometric mean          | (ref)                                                   | 1.00x faster                                                          |

Benchmark hidden because not significant (56): async_tree_memoization, xml_etree_iterparse, async_tree_cpu_io_mixed, xml_etree_generate, html5lib, async_tree_memoization_tg, deltablue, raytrace, nqueens, json_dumps, nbody, async_tree_cpu_io_mixed_tg, mdp, async_generators, create_gc_cycles, fannkuch, spectral_norm, pickle_list, pidigits, scimark_sor, asyncio_websockets, pickle_dict, scimark_monte_carlo, asyncio_tcp_ssl, unpickle_pure_python, scimark_fft, richards_super, sqlglot_normalize, pickle, xml_etree_process, sqlite_synth, genshi_text, telco, typing_runtime_protocols, pylint, 2to3, go, pathlib, sympy_str, python_startup_no_site, unpickle, hexiom, scimark_lu, unpickle_list, django_template, thrift, pyflate, json, sqlglot_transpile, float, json_loads, chaos, tornado_http, sqlglot_parse, richards, genshi_xml
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 77.09% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x