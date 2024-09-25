# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.02x slower
- HPT reliability: 98.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 4.01 sec                                                | 4.12 sec: 1.03x slower                                |
| html5lib       | 98.1 ms                                                 | 89.1 ms: 1.10x faster                                 |
| tornado_http   | 248 ms                                                  | 270 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                   | 1.01x slower                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 576 ms                                                  | 502 ms: 1.15x faster                                  |
| async_tree_memoization     | 745 ms                                                  | 686 ms: 1.09x faster                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 887 ms: 1.04x slower                                  |
| coroutines                 | 29.2 ms                                                 | 30.8 ms: 1.05x slower                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 2.99 sec: 1.07x slower                                |
| Geometric mean             | (ref)                                                   | 1.01x faster                                          |

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed, async_generators, async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp, async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 297 ms: 1.03x slower                                  |
| regex_compile  | 177 ms                                                  | 193 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                   | 1.03x slower                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|--------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle           | 21.4 us                                                 | 19.9 us: 1.07x faster                                 |
| pickle_dict        | 46.5 us                                                 | 49.2 us: 1.06x slower                                 |
| pickle             | 15.4 us                                                 | 16.6 us: 1.08x slower                                 |
| unpickle_list      | 6.67 us                                                 | 7.33 us: 1.10x slower                                 |
| pickle_pure_python | 417 us                                                  | 458 us: 1.10x slower                                  |
| pickle_list        | 6.82 us                                                 | 7.57 us: 1.11x slower                                 |
| json_loads         | 36.1 us                                                 | 41.2 us: 1.14x slower                                 |
| Geometric mean     | (ref)                                                   | 1.02x slower                                          |

Benchmark hidden because not significant (7): xml_etree_process, xml_etree_iterparse, json_dumps, xml_etree_generate, xml_etree_parse, unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 25.6 ms: 1.16x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 17.8 ms: 1.22x slower                                 |
| Geometric mean         | (ref)                                                   | 1.19x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.7 ms                                                 | 34.1 ms: 1.07x slower                                 |
| genshi_xml     | 68.3 ms                                                 | 76.1 ms: 1.11x slower                                 |
| mako           | 16.1 ms                                                 | 19.0 ms: 1.18x slower                                 |
| Geometric mean | (ref)                                                   | 1.10x slower                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy                   | 484 us                                                  | 341 us: 1.42x faster                                  |
| deepcopy_memo              | 51.7 us                                                 | 39.8 us: 1.30x faster                                 |
| unpack_sequence            | 73.9 ns                                                 | 62.2 ns: 1.19x faster                                 |
| deepcopy_reduce            | 4.27 us                                                 | 3.61 us: 1.18x faster                                 |
| async_tree_none            | 576 ms                                                  | 502 ms: 1.15x faster                                  |
| go                         | 195 ms                                                  | 171 ms: 1.15x faster                                  |
| html5lib                   | 98.1 ms                                                 | 89.1 ms: 1.10x faster                                 |
| async_tree_memoization     | 745 ms                                                  | 686 ms: 1.09x faster                                  |
| unpickle                   | 21.4 us                                                 | 19.9 us: 1.07x faster                                 |
| crypto_pyaes               | 99.8 ms                                                 | 93.8 ms: 1.06x faster                                 |
| richards                   | 65.8 ms                                                 | 63.3 ms: 1.04x faster                                 |
| docutils                   | 4.01 sec                                                | 4.12 sec: 1.03x slower                                |
| regex_dna                  | 288 ms                                                  | 297 ms: 1.03x slower                                  |
| bpe_tokeniser              | 6.25 sec                                                | 6.49 sec: 1.04x slower                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 887 ms: 1.04x slower                                  |
| scimark_fft                | 477 ms                                                  | 499 ms: 1.05x slower                                  |
| pprint_safe_repr           | 959 ms                                                  | 1.01 sec: 1.05x slower                                |
| coroutines                 | 29.2 ms                                                 | 30.8 ms: 1.05x slower                                 |
| pickle_dict                | 46.5 us                                                 | 49.2 us: 1.06x slower                                 |
| pycparser                  | 1.57 sec                                                | 1.67 sec: 1.06x slower                                |
| coverage                   | 110 ms                                                  | 117 ms: 1.06x slower                                  |
| generators                 | 39.2 ms                                                 | 41.7 ms: 1.06x slower                                 |
| nqueens                    | 108 ms                                                  | 116 ms: 1.07x slower                                  |
| asyncio_tcp_ssl            | 2.79 sec                                                | 2.99 sec: 1.07x slower                                |
| genshi_text                | 31.7 ms                                                 | 34.1 ms: 1.07x slower                                 |
| gc_traversal               | 5.91 ms                                                 | 6.35 ms: 1.07x slower                                 |
| mdp                        | 3.80 sec                                                | 4.09 sec: 1.08x slower                                |
| pickle                     | 15.4 us                                                 | 16.6 us: 1.08x slower                                 |
| regex_compile              | 177 ms                                                  | 193 ms: 1.09x slower                                  |
| tornado_http               | 248 ms                                                  | 270 ms: 1.09x slower                                  |
| comprehensions             | 20.9 us                                                 | 23.0 us: 1.10x slower                                 |
| create_gc_cycles           | 2.46 ms                                                 | 2.70 ms: 1.10x slower                                 |
| unpickle_list              | 6.67 us                                                 | 7.33 us: 1.10x slower                                 |
| pickle_pure_python         | 417 us                                                  | 458 us: 1.10x slower                                  |
| pickle_list                | 6.82 us                                                 | 7.57 us: 1.11x slower                                 |
| json                       | 6.55 ms                                                 | 7.28 ms: 1.11x slower                                 |
| genshi_xml                 | 68.3 ms                                                 | 76.1 ms: 1.11x slower                                 |
| logging_silent             | 130 ns                                                  | 146 ns: 1.13x slower                                  |
| sqlglot_parse              | 1.80 ms                                                 | 2.03 ms: 1.13x slower                                 |
| logging_format             | 9.48 us                                                 | 10.7 us: 1.13x slower                                 |
| json_loads                 | 36.1 us                                                 | 41.2 us: 1.14x slower                                 |
| python_startup             | 22.0 ms                                                 | 25.6 ms: 1.16x slower                                 |
| bench_mp_pool              | 19.4 ms                                                 | 22.8 ms: 1.18x slower                                 |
| mako                       | 16.1 ms                                                 | 19.0 ms: 1.18x slower                                 |
| python_startup_no_site     | 14.6 ms                                                 | 17.8 ms: 1.22x slower                                 |
| bench_thread_pool          | 3.06 ms                                                 | 3.86 ms: 1.26x slower                                 |
| Geometric mean             | (ref)                                                   | 1.02x slower                                          |

Benchmark hidden because not significant (51): async_tree_io_tg, xml_etree_process, sqlglot_transpile, xml_etree_iterparse, richards_super, json_dumps, meteor_contest, xml_etree_generate, thrift, chaos, logging_simple, nbody, sqlite_synth, sympy_expand, async_tree_cpu_io_mixed, xml_etree_parse, async_generators, regex_v8, scimark_sparse_mat_mult, pprint_pformat, async_tree_memoization_tg, unpickle_pure_python, async_tree_none_tg, pidigits, sqlglot_optimize, deltablue, sympy_integrate, spectral_norm, asyncio_tcp, dulwich_log, async_tree_io, scimark_sor, sqlglot_normalize, 2to3, tomli_loads, scimark_lu, sympy_str, asyncio_websockets, fannkuch, scimark_monte_carlo, pathlib, typing_runtime_protocols, regex_effbot, hexiom, raytrace, django_template, telco, float, sympy_sum, pyflate, pylint
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 98.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x