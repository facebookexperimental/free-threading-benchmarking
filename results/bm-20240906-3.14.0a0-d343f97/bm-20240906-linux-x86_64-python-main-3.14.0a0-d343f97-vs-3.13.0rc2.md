# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.03x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 4.12 sec: 1.03x slower                                |
| tornado_http   | 251 ms                                                       | 270 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                          |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 502 ms: 1.14x faster                                  |
| async_generators           | 567 ms                                                       | 586 ms: 1.03x slower                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 887 ms: 1.04x slower                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.99 sec: 1.08x slower                                |
| Geometric mean             | (ref)                                                        | 1.01x slower                                          |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg, coroutines, async_tree_cpu_io_mixed, async_tree_io, asyncio_websockets, async_tree_none_tg, asyncio_tcp

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.96 ms: 1.05x slower                                 |
| regex_dna      | 282 ms                                                       | 297 ms: 1.06x slower                                  |
| regex_compile  | 182 ms                                                       | 193 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|--------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_list      | 6.68 us                                                      | 7.33 us: 1.10x slower                                 |
| pickle_pure_python | 416 us                                                       | 458 us: 1.10x slower                                  |
| pickle             | 15.1 us                                                      | 16.6 us: 1.10x slower                                 |
| pickle_list        | 6.86 us                                                      | 7.57 us: 1.10x slower                                 |
| json_loads         | 34.3 us                                                      | 41.2 us: 1.20x slower                                 |
| Geometric mean     | (ref)                                                        | 1.04x slower                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, xml_etree_process, unpickle, xml_etree_parse, unpickle_pure_python, tomli_loads, json_dumps, xml_etree_generate, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 25.6 ms: 1.14x slower                                 |
| python_startup_no_site | 15.3 ms                                                      | 17.8 ms: 1.16x slower                                 |
| Geometric mean         | (ref)                                                        | 1.15x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 34.1 ms: 1.08x slower                                 |
| django_template | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                 |
| mako            | 15.9 ms                                                      | 19.0 ms: 1.19x slower                                 |
| Geometric mean  | (ref)                                                        | 1.10x slower                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy                   | 498 us                                                       | 341 us: 1.46x faster                                  |
| deepcopy_memo              | 50.1 us                                                      | 39.8 us: 1.26x faster                                 |
| unpack_sequence            | 74.3 ns                                                      | 62.2 ns: 1.19x faster                                 |
| async_tree_none            | 572 ms                                                       | 502 ms: 1.14x faster                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.61 us: 1.14x faster                                 |
| go                         | 191 ms                                                       | 171 ms: 1.12x faster                                  |
| crypto_pyaes               | 100 ms                                                       | 93.8 ms: 1.07x faster                                 |
| docutils                   | 4.01 sec                                                     | 4.12 sec: 1.03x slower                                |
| async_generators           | 567 ms                                                       | 586 ms: 1.03x slower                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.49 sec: 1.03x slower                                |
| pyflate                    | 664 ms                                                       | 690 ms: 1.04x slower                                  |
| generators                 | 40.0 ms                                                      | 41.7 ms: 1.04x slower                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 887 ms: 1.04x slower                                  |
| regex_effbot               | 4.74 ms                                                      | 4.96 ms: 1.05x slower                                 |
| raytrace                   | 344 ms                                                       | 361 ms: 1.05x slower                                  |
| scimark_fft                | 473 ms                                                       | 499 ms: 1.05x slower                                  |
| sqlglot_normalize          | 140 ms                                                       | 148 ms: 1.06x slower                                  |
| regex_dna                  | 282 ms                                                       | 297 ms: 1.06x slower                                  |
| hexiom                     | 8.11 ms                                                      | 8.58 ms: 1.06x slower                                 |
| regex_compile              | 182 ms                                                       | 193 ms: 1.06x slower                                  |
| sympy_sum                  | 210 ms                                                       | 222 ms: 1.06x slower                                  |
| pycparser                  | 1.57 sec                                                     | 1.67 sec: 1.06x slower                                |
| scimark_lu                 | 146 ms                                                       | 156 ms: 1.07x slower                                  |
| tornado_http               | 251 ms                                                       | 270 ms: 1.07x slower                                  |
| dulwich_log                | 93.7 ms                                                      | 101 ms: 1.07x slower                                  |
| genshi_text                | 31.7 ms                                                      | 34.1 ms: 1.08x slower                                 |
| mdp                        | 3.80 sec                                                     | 4.09 sec: 1.08x slower                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.99 sec: 1.08x slower                                |
| coverage                   | 107 ms                                                       | 117 ms: 1.09x slower                                  |
| django_template            | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                 |
| unpickle_list              | 6.68 us                                                      | 7.33 us: 1.10x slower                                 |
| pickle_pure_python         | 416 us                                                       | 458 us: 1.10x slower                                  |
| pickle                     | 15.1 us                                                      | 16.6 us: 1.10x slower                                 |
| pickle_list                | 6.86 us                                                      | 7.57 us: 1.10x slower                                 |
| gc_traversal               | 5.70 ms                                                      | 6.35 ms: 1.11x slower                                 |
| json                       | 6.51 ms                                                      | 7.28 ms: 1.12x slower                                 |
| create_gc_cycles           | 2.41 ms                                                      | 2.70 ms: 1.12x slower                                 |
| logging_silent             | 130 ns                                                       | 146 ns: 1.13x slower                                  |
| python_startup             | 22.4 ms                                                      | 25.6 ms: 1.14x slower                                 |
| sqlglot_parse              | 1.76 ms                                                      | 2.03 ms: 1.16x slower                                 |
| logging_format             | 9.24 us                                                      | 10.7 us: 1.16x slower                                 |
| python_startup_no_site     | 15.3 ms                                                      | 17.8 ms: 1.16x slower                                 |
| mako                       | 15.9 ms                                                      | 19.0 ms: 1.19x slower                                 |
| json_loads                 | 34.3 us                                                      | 41.2 us: 1.20x slower                                 |
| bench_mp_pool              | 18.7 ms                                                      | 22.8 ms: 1.22x slower                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.86 ms: 1.34x slower                                 |
| Geometric mean             | (ref)                                                        | 1.03x slower                                          |

Benchmark hidden because not significant (51): xml_etree_iterparse, html5lib, xml_etree_process, richards, async_tree_memoization, unpickle, telco, scimark_sor, regex_v8, typing_runtime_protocols, pidigits, sympy_integrate, sympy_str, thrift, chaos, async_tree_io_tg, async_tree_memoization_tg, coroutines, async_tree_cpu_io_mixed, pathlib, async_tree_io, 2to3, sqlglot_transpile, richards_super, sqlite_synth, fannkuch, xml_etree_parse, scimark_monte_carlo, unpickle_pure_python, meteor_contest, sqlglot_optimize, pprint_pformat, tomli_loads, json_dumps, pprint_safe_repr, spectral_norm, xml_etree_generate, asyncio_websockets, scimark_sparse_mat_mult, logging_simple, nbody, deltablue, async_tree_none_tg, comprehensions, float, nqueens, sympy_expand, pickle_dict, asyncio_tcp, genshi_xml, pylint
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x