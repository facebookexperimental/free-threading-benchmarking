# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 415 ms: 1.06x faster                                  |
| docutils       | 4.01 sec                                                | 3.82 sec: 1.05x faster                                |
| html5lib       | 98.1 ms                                                 | 88.4 ms: 1.11x faster                                 |
| Geometric mean | (ref)                                                   | 1.06x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization    | 745 ms                                                  | 637 ms: 1.17x faster                                  |
| async_tree_none           | 576 ms                                                  | 501 ms: 1.15x faster                                  |
| async_tree_io_tg          | 1.46 sec                                                | 1.32 sec: 1.11x faster                                |
| asyncio_tcp               | 985 ms                                                  | 901 ms: 1.09x faster                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 823 ms: 1.09x faster                                  |
| async_tree_memoization_tg | 672 ms                                                  | 621 ms: 1.08x faster                                  |
| async_tree_none_tg        | 521 ms                                                  | 483 ms: 1.08x faster                                  |
| async_generators          | 592 ms                                                  | 575 ms: 1.03x faster                                  |
| asyncio_websockets        | 772 ms                                                  | 751 ms: 1.03x faster                                  |
| asyncio_tcp_ssl           | 2.79 sec                                                | 2.73 sec: 1.02x faster                                |
| coroutines                | 29.2 ms                                                 | 32.0 ms: 1.10x slower                                 |
| Geometric mean            | (ref)                                                   | 1.06x faster                                          |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 124 ms                                                  | 116 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                   | 1.01x faster                                          |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 5.19 ms: 1.07x slower                                 |
| regex_v8       | 32.4 ms                                                 | 34.9 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                   | 1.03x slower                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|--------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate | 129 ms                                                  | 118 ms: 1.09x faster                                  |
| pickle_dict        | 46.5 us                                                 | 44.6 us: 1.04x faster                                 |
| json_loads         | 36.1 us                                                 | 37.9 us: 1.05x slower                                 |
| json_dumps         | 14.9 ms                                                 | 15.8 ms: 1.06x slower                                 |
| pickle             | 15.4 us                                                 | 16.5 us: 1.08x slower                                 |
| unpickle_list      | 6.67 us                                                 | 7.20 us: 1.08x slower                                 |
| Geometric mean     | (ref)                                                   | 1.00x slower                                          |

Benchmark hidden because not significant (8): xml_etree_iterparse, unpickle, unpickle_pure_python, tomli_loads, xml_etree_parse, xml_etree_process, pickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.7 ms                                                 | 33.6 ms: 1.06x slower                                 |
| mako           | 16.1 ms                                                 | 18.2 ms: 1.13x slower                                 |
| Geometric mean | (ref)                                                   | 1.04x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| unpack_sequence           | 73.9 ns                                                 | 51.6 ns: 1.43x faster                                 |
| deepcopy                  | 484 us                                                  | 354 us: 1.37x faster                                  |
| go                        | 195 ms                                                  | 161 ms: 1.22x faster                                  |
| deepcopy_memo             | 51.7 us                                                 | 43.0 us: 1.20x faster                                 |
| deepcopy_reduce           | 4.27 us                                                 | 3.62 us: 1.18x faster                                 |
| async_tree_memoization    | 745 ms                                                  | 637 ms: 1.17x faster                                  |
| scimark_sparse_mat_mult   | 6.98 ms                                                 | 6.07 ms: 1.15x faster                                 |
| async_tree_none           | 576 ms                                                  | 501 ms: 1.15x faster                                  |
| html5lib                  | 98.1 ms                                                 | 88.4 ms: 1.11x faster                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.32 sec: 1.11x faster                                |
| sympy_integrate           | 29.7 ms                                                 | 27.0 ms: 1.10x faster                                 |
| xml_etree_generate        | 129 ms                                                  | 118 ms: 1.09x faster                                  |
| asyncio_tcp               | 985 ms                                                  | 901 ms: 1.09x faster                                  |
| spectral_norm             | 159 ms                                                  | 146 ms: 1.09x faster                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 823 ms: 1.09x faster                                  |
| async_tree_memoization_tg | 672 ms                                                  | 621 ms: 1.08x faster                                  |
| async_tree_none_tg        | 521 ms                                                  | 483 ms: 1.08x faster                                  |
| sqlglot_transpile         | 2.30 ms                                                 | 2.13 ms: 1.08x faster                                 |
| nbody                     | 124 ms                                                  | 116 ms: 1.07x faster                                  |
| richards_super            | 76.3 ms                                                 | 71.4 ms: 1.07x faster                                 |
| thrift                    | 1.11 ms                                                 | 1.05 ms: 1.07x faster                                 |
| 2to3                      | 442 ms                                                  | 415 ms: 1.06x faster                                  |
| sqlglot_parse             | 1.80 ms                                                 | 1.69 ms: 1.06x faster                                 |
| meteor_contest            | 157 ms                                                  | 148 ms: 1.06x faster                                  |
| sqlite_synth              | 4.07 us                                                 | 3.86 us: 1.06x faster                                 |
| pprint_pformat            | 2.00 sec                                                | 1.89 sec: 1.06x faster                                |
| sqlglot_optimize          | 76.2 ms                                                 | 72.3 ms: 1.05x faster                                 |
| gc_traversal              | 5.91 ms                                                 | 5.62 ms: 1.05x faster                                 |
| docutils                  | 4.01 sec                                                | 3.82 sec: 1.05x faster                                |
| scimark_monte_carlo       | 89.9 ms                                                 | 85.8 ms: 1.05x faster                                 |
| sympy_expand              | 631 ms                                                  | 603 ms: 1.05x faster                                  |
| pprint_safe_repr          | 959 ms                                                  | 916 ms: 1.05x faster                                  |
| pickle_dict               | 46.5 us                                                 | 44.6 us: 1.04x faster                                 |
| sqlglot_normalize         | 146 ms                                                  | 140 ms: 1.04x faster                                  |
| async_generators          | 592 ms                                                  | 575 ms: 1.03x faster                                  |
| asyncio_websockets        | 772 ms                                                  | 751 ms: 1.03x faster                                  |
| asyncio_tcp_ssl           | 2.79 sec                                                | 2.73 sec: 1.02x faster                                |
| bpe_tokeniser             | 6.25 sec                                                | 6.12 sec: 1.02x faster                                |
| json_loads                | 36.1 us                                                 | 37.9 us: 1.05x slower                                 |
| mdp                       | 3.80 sec                                                | 3.99 sec: 1.05x slower                                |
| json                      | 6.55 ms                                                 | 6.88 ms: 1.05x slower                                 |
| comprehensions            | 20.9 us                                                 | 22.0 us: 1.05x slower                                 |
| nqueens                   | 108 ms                                                  | 114 ms: 1.05x slower                                  |
| genshi_text               | 31.7 ms                                                 | 33.6 ms: 1.06x slower                                 |
| json_dumps                | 14.9 ms                                                 | 15.8 ms: 1.06x slower                                 |
| regex_effbot              | 4.84 ms                                                 | 5.19 ms: 1.07x slower                                 |
| pickle                    | 15.4 us                                                 | 16.5 us: 1.08x slower                                 |
| regex_v8                  | 32.4 ms                                                 | 34.9 ms: 1.08x slower                                 |
| unpickle_list             | 6.67 us                                                 | 7.20 us: 1.08x slower                                 |
| coroutines                | 29.2 ms                                                 | 32.0 ms: 1.10x slower                                 |
| generators                | 39.2 ms                                                 | 43.6 ms: 1.11x slower                                 |
| mako                      | 16.1 ms                                                 | 18.2 ms: 1.13x slower                                 |
| dulwich_log               | 100.0 ms                                                | 123 ms: 1.23x slower                                  |
| Geometric mean            | (ref)                                                   | 1.03x faster                                          |

Benchmark hidden because not significant (44): xml_etree_iterparse, create_gc_cycles, hexiom, sympy_sum, unpickle, raytrace, django_template, unpickle_pure_python, sympy_str, coverage, scimark_fft, python_startup, scimark_sor, chaos, tomli_loads, pycparser, xml_etree_parse, crypto_pyaes, richards, regex_compile, async_tree_io, fannkuch, tornado_http, telco, xml_etree_process, float, regex_dna, scimark_lu, deltablue, async_tree_cpu_io_mixed_tg, pathlib, pylint, logging_silent, genshi_xml, pickle_list, pyflate, python_startup_no_site, pidigits, typing_runtime_protocols, logging_format, logging_simple, pickle_pure_python, bench_thread_pool, bench_mp_pool
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x