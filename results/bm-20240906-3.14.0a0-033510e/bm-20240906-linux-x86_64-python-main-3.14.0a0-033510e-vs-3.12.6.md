# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 415 ms: 1.10x faster                                  |
| docutils       | 4.00 sec                                               | 3.82 sec: 1.05x faster                                |
| tornado_http   | 266 ms                                                 | 246 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 637 ms: 1.53x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 621 ms: 1.50x faster                                  |
| async_tree_none            | 741 ms                                                 | 501 ms: 1.48x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.32 sec: 1.47x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 483 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.36 sec: 1.36x faster                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 823 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 853 ms: 1.29x faster                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.73 sec: 1.03x faster                                |
| async_generators           | 589 ms                                                 | 575 ms: 1.02x faster                                  |
| coroutines                 | 29.5 ms                                                | 32.0 ms: 1.08x slower                                 |
| Geometric mean             | (ref)                                                  | 1.24x faster                                          |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                          |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 175 ms: 1.06x faster                                  |
| regex_dna      | 278 ms                                                 | 288 ms: 1.03x slower                                  |
| regex_v8       | 32.5 ms                                                | 34.9 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|--------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict        | 52.7 us                                                | 44.6 us: 1.18x faster                                 |
| xml_etree_generate | 127 ms                                                 | 118 ms: 1.08x faster                                  |
| tomli_loads        | 2.88 sec                                               | 2.75 sec: 1.05x faster                                |
| unpickle_list      | 6.83 us                                                | 7.20 us: 1.05x slower                                 |
| json_dumps         | 14.3 ms                                                | 15.8 ms: 1.11x slower                                 |
| Geometric mean     | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (9): unpickle_pure_python, xml_etree_parse, unpickle, xml_etree_iterparse, pickle_list, pickle_pure_python, json_loads, pickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.1 ms: 1.17x faster                                 |
| python_startup         | 23.7 ms                                                | 21.6 ms: 1.10x faster                                 |
| Geometric mean         | (ref)                                                  | 1.13x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 33.6 ms: 1.11x slower                                 |
| mako           | 15.7 ms                                                | 18.2 ms: 1.16x slower                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 637 ms: 1.53x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 621 ms: 1.50x faster                                  |
| async_tree_none            | 741 ms                                                 | 501 ms: 1.48x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.32 sec: 1.47x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 483 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.36 sec: 1.36x faster                                |
| deepcopy                   | 468 us                                                 | 354 us: 1.32x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 823 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 853 ms: 1.29x faster                                  |
| comprehensions             | 27.1 us                                                | 22.0 us: 1.23x faster                                 |
| deepcopy_memo              | 52.4 us                                                | 43.0 us: 1.22x faster                                 |
| raytrace                   | 408 ms                                                 | 340 ms: 1.20x faster                                  |
| pickle_dict                | 52.7 us                                                | 44.6 us: 1.18x faster                                 |
| python_startup_no_site     | 17.6 ms                                                | 15.1 ms: 1.17x faster                                 |
| unpack_sequence            | 60.2 ns                                                | 51.6 ns: 1.17x faster                                 |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                |
| scimark_monte_carlo        | 96.4 ms                                                | 85.8 ms: 1.12x faster                                 |
| sqlglot_normalize          | 157 ms                                                 | 140 ms: 1.12x faster                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.62 us: 1.12x faster                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.07 ms: 1.10x faster                                 |
| sympy_integrate            | 29.8 ms                                                | 27.0 ms: 1.10x faster                                 |
| 2to3                       | 456 ms                                                 | 415 ms: 1.10x faster                                  |
| python_startup             | 23.7 ms                                                | 21.6 ms: 1.10x faster                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.13 ms: 1.09x faster                                 |
| crypto_pyaes               | 107 ms                                                 | 98.5 ms: 1.09x faster                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.22 ms: 1.08x faster                                 |
| tornado_http               | 266 ms                                                 | 246 ms: 1.08x faster                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.12 sec: 1.08x faster                                |
| xml_etree_generate         | 127 ms                                                 | 118 ms: 1.08x faster                                  |
| pyflate                    | 727 ms                                                 | 676 ms: 1.08x faster                                  |
| sympy_str                  | 385 ms                                                 | 358 ms: 1.07x faster                                  |
| float                      | 123 ms                                                 | 115 ms: 1.07x faster                                  |
| go                         | 172 ms                                                 | 161 ms: 1.07x faster                                  |
| scimark_fft                | 500 ms                                                 | 467 ms: 1.07x faster                                  |
| sympy_sum                  | 222 ms                                                 | 207 ms: 1.07x faster                                  |
| spectral_norm              | 156 ms                                                 | 146 ms: 1.07x faster                                  |
| pathlib                    | 31.6 ms                                                | 29.7 ms: 1.06x faster                                 |
| regex_compile              | 187 ms                                                 | 175 ms: 1.06x faster                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.69 ms: 1.06x faster                                 |
| pprint_safe_repr           | 967 ms                                                 | 916 ms: 1.06x faster                                  |
| logging_silent             | 139 ns                                                 | 132 ns: 1.05x faster                                  |
| sqlglot_optimize           | 76.0 ms                                                | 72.3 ms: 1.05x faster                                 |
| tomli_loads                | 2.88 sec                                               | 2.75 sec: 1.05x faster                                |
| pprint_pformat             | 1.98 sec                                               | 1.89 sec: 1.05x faster                                |
| docutils                   | 4.00 sec                                               | 3.82 sec: 1.05x faster                                |
| gc_traversal               | 5.86 ms                                                | 5.62 ms: 1.04x faster                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.73 sec: 1.03x faster                                |
| async_generators           | 589 ms                                                 | 575 ms: 1.02x faster                                  |
| regex_dna                  | 278 ms                                                 | 288 ms: 1.03x slower                                  |
| unpickle_list              | 6.83 us                                                | 7.20 us: 1.05x slower                                 |
| generators                 | 41.1 ms                                                | 43.6 ms: 1.06x slower                                 |
| deltablue                  | 4.27 ms                                                | 4.57 ms: 1.07x slower                                 |
| regex_v8                   | 32.5 ms                                                | 34.9 ms: 1.08x slower                                 |
| richards                   | 60.3 ms                                                | 65.0 ms: 1.08x slower                                 |
| coroutines                 | 29.5 ms                                                | 32.0 ms: 1.08x slower                                 |
| json_dumps                 | 14.3 ms                                                | 15.8 ms: 1.11x slower                                 |
| genshi_text                | 30.2 ms                                                | 33.6 ms: 1.11x slower                                 |
| coverage                   | 95.4 ms                                                | 107 ms: 1.13x slower                                  |
| mako                       | 15.7 ms                                                | 18.2 ms: 1.16x slower                                 |
| telco                      | 9.59 ms                                                | 11.3 ms: 1.18x slower                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.35 ms: 1.21x slower                                 |
| dulwich_log                | 100 ms                                                 | 123 ms: 1.22x slower                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                          |

Benchmark hidden because not significant (35): unpickle_pure_python, xml_etree_parse, nbody, nqueens, asyncio_tcp, hexiom, unpickle, chaos, richards_super, xml_etree_iterparse, bench_mp_pool, thrift, logging_simple, html5lib, typing_runtime_protocols, fannkuch, sqlite_synth, pickle_list, pickle_pure_python, json_loads, asyncio_websockets, mdp, json, pickle, regex_effbot, meteor_contest, scimark_sor, scimark_lu, django_template, pidigits, logging_format, genshi_xml, pylint, xml_etree_process, sympy_expand
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x