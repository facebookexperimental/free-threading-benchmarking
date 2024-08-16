# Results vs. 3.13.0rc1+

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| html5lib       | 98.1 ms                                                 | 93.1 ms: 1.05x faster                                                 |
| tornado_http   | 248 ms                                                  | 228 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                   | 1.05x faster                                                          |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.22 sec: 1.19x faster                                                |
| async_tree_memoization     | 745 ms                                                  | 626 ms: 1.19x faster                                                  |
| async_tree_none_tg         | 521 ms                                                  | 451 ms: 1.15x faster                                                  |
| async_tree_none            | 576 ms                                                  | 499 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 672 ms                                                  | 591 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 794 ms: 1.13x faster                                                  |
| async_tree_io              | 1.38 sec                                                | 1.26 sec: 1.09x faster                                                |
| asyncio_tcp                | 985 ms                                                  | 928 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 806 ms: 1.05x faster                                                  |
| asyncio_websockets         | 772 ms                                                  | 746 ms: 1.03x faster                                                  |
| coroutines                 | 29.2 ms                                                 | 31.6 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                   | 1.09x faster                                                          |

Benchmark hidden because not significant (2): async_generators, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 35.8 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                   | 1.01x slower                                                          |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|---------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 176 ms                                                  | 158 ms: 1.12x faster                                                  |
| xml_etree_generate  | 129 ms                                                  | 117 ms: 1.10x faster                                                  |
| pickle_list         | 6.82 us                                                 | 6.33 us: 1.08x faster                                                 |
| unpickle            | 21.4 us                                                 | 19.8 us: 1.08x faster                                                 |
| xml_etree_process   | 86.5 ms                                                 | 81.3 ms: 1.06x faster                                                 |
| tomli_loads         | 2.80 sec                                                | 2.66 sec: 1.05x faster                                                |
| unpickle_list       | 6.67 us                                                 | 7.22 us: 1.08x slower                                                 |
| Geometric mean      | (ref)                                                   | 1.02x faster                                                          |

Benchmark hidden because not significant (7): xml_etree_parse, pickle_dict, pickle, json_loads, unpickle_pure_python, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 46.9 ms                                                 | 44.0 ms: 1.07x faster                                                 |
| genshi_text     | 31.7 ms                                                 | 30.2 ms: 1.05x faster                                                 |
| genshi_xml      | 68.3 ms                                                 | 73.3 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.01x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy_memo              | 51.7 us                                                 | 38.4 us: 1.35x faster                                                 |
| deepcopy                   | 484 us                                                  | 372 us: 1.30x faster                                                  |
| async_tree_io_tg           | 1.46 sec                                                | 1.22 sec: 1.19x faster                                                |
| async_tree_memoization     | 745 ms                                                  | 626 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 4.27 us                                                 | 3.64 us: 1.17x faster                                                 |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 5.99 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 521 ms                                                  | 451 ms: 1.15x faster                                                  |
| async_tree_none            | 576 ms                                                  | 499 ms: 1.15x faster                                                  |
| richards_super             | 76.3 ms                                                 | 66.2 ms: 1.15x faster                                                 |
| async_tree_memoization_tg  | 672 ms                                                  | 591 ms: 1.14x faster                                                  |
| meteor_contest             | 157 ms                                                  | 138 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 794 ms: 1.13x faster                                                  |
| logging_simple             | 8.98 us                                                 | 7.95 us: 1.13x faster                                                 |
| xml_etree_iterparse        | 176 ms                                                  | 158 ms: 1.12x faster                                                  |
| deltablue                  | 4.56 ms                                                 | 4.11 ms: 1.11x faster                                                 |
| xml_etree_generate         | 129 ms                                                  | 117 ms: 1.10x faster                                                  |
| pathlib                    | 29.3 ms                                                 | 26.6 ms: 1.10x faster                                                 |
| unpack_sequence            | 73.9 ns                                                 | 67.4 ns: 1.10x faster                                                 |
| async_tree_io              | 1.38 sec                                                | 1.26 sec: 1.09x faster                                                |
| tornado_http               | 248 ms                                                  | 228 ms: 1.09x faster                                                  |
| sqlglot_transpile          | 2.30 ms                                                 | 2.12 ms: 1.09x faster                                                 |
| gc_traversal               | 5.91 ms                                                 | 5.48 ms: 1.08x faster                                                 |
| pickle_list                | 6.82 us                                                 | 6.33 us: 1.08x faster                                                 |
| unpickle                   | 21.4 us                                                 | 19.8 us: 1.08x faster                                                 |
| chaos                      | 84.7 ms                                                 | 79.1 ms: 1.07x faster                                                 |
| django_template            | 46.9 ms                                                 | 44.0 ms: 1.07x faster                                                 |
| sympy_expand               | 631 ms                                                  | 591 ms: 1.07x faster                                                  |
| sympy_str                  | 367 ms                                                  | 345 ms: 1.06x faster                                                  |
| xml_etree_process          | 86.5 ms                                                 | 81.3 ms: 1.06x faster                                                 |
| sqlglot_parse              | 1.80 ms                                                 | 1.69 ms: 1.06x faster                                                 |
| asyncio_tcp                | 985 ms                                                  | 928 ms: 1.06x faster                                                  |
| logging_format             | 9.48 us                                                 | 8.93 us: 1.06x faster                                                 |
| create_gc_cycles           | 2.46 ms                                                 | 2.32 ms: 1.06x faster                                                 |
| spectral_norm              | 159 ms                                                  | 150 ms: 1.06x faster                                                  |
| tomli_loads                | 2.80 sec                                                | 2.66 sec: 1.05x faster                                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 806 ms: 1.05x faster                                                  |
| html5lib                   | 98.1 ms                                                 | 93.1 ms: 1.05x faster                                                 |
| genshi_text                | 31.7 ms                                                 | 30.2 ms: 1.05x faster                                                 |
| telco                      | 11.4 ms                                                 | 10.9 ms: 1.04x faster                                                 |
| mdp                        | 3.80 sec                                                | 3.64 sec: 1.04x faster                                                |
| asyncio_websockets         | 772 ms                                                  | 746 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 6.25 sec                                                | 6.13 sec: 1.02x faster                                                |
| pycparser                  | 1.57 sec                                                | 1.63 sec: 1.04x slower                                                |
| coverage                   | 110 ms                                                  | 118 ms: 1.07x slower                                                  |
| genshi_xml                 | 68.3 ms                                                 | 73.3 ms: 1.07x slower                                                 |
| coroutines                 | 29.2 ms                                                 | 31.6 ms: 1.08x slower                                                 |
| unpickle_list              | 6.67 us                                                 | 7.22 us: 1.08x slower                                                 |
| typing_runtime_protocols   | 216 us                                                  | 234 us: 1.08x slower                                                  |
| nqueens                    | 108 ms                                                  | 117 ms: 1.09x slower                                                  |
| regex_v8                   | 32.4 ms                                                 | 35.8 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                   | 1.04x faster                                                          |

Benchmark hidden because not significant (47): sympy_integrate, nbody, go, 2to3, richards, raytrace, bench_thread_pool, scimark_monte_carlo, sympy_sum, xml_etree_parse, pprint_pformat, scimark_sor, float, async_generators, pidigits, regex_dna, bench_mp_pool, regex_compile, asyncio_tcp_ssl, logging_silent, docutils, regex_effbot, fannkuch, scimark_fft, sqlglot_normalize, thrift, pyflate, comprehensions, dask, crypto_pyaes, generators, python_startup, scimark_lu, pickle_dict, pylint, pprint_safe_repr, sqlite_synth, pickle, mako, sqlglot_optimize, hexiom, json, python_startup_no_site, json_loads, unpickle_pure_python, pickle_pure_python, json_dumps
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x