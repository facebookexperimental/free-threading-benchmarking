# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.88x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 415 ms: 1.07x faster                                  |
| docutils       | 4.06 sec                                                              | 3.82 sec: 1.06x faster                                |
| html5lib       | 95.8 ms                                                               | 88.4 ms: 1.08x faster                                 |
| Geometric mean | (ref)                                                                 | 1.07x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 621 ms: 1.51x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 637 ms: 1.49x faster                                  |
| async_tree_none            | 740 ms                                                                | 501 ms: 1.48x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 483 ms: 1.43x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 823 ms: 1.38x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.32 sec: 1.37x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.36 sec: 1.31x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 853 ms: 1.29x faster                                  |
| async_generators           | 617 ms                                                                | 575 ms: 1.07x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 901 ms: 1.06x faster                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.73 sec: 1.03x faster                                |
| coroutines                 | 30.1 ms                                                               | 32.0 ms: 1.06x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.24x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 115 ms: 1.10x faster                                  |
| nbody          | 125 ms                                                                | 116 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                                 | 1.06x faster                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 175 ms: 1.12x faster                                  |
| regex_effbot   | 4.97 ms                                                               | 5.19 ms: 1.04x slower                                 |
| regex_v8       | 31.1 ms                                                               | 34.9 ms: 1.12x slower                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_pure_python | 319 us                                                                | 288 us: 1.11x faster                                  |
| xml_etree_generate   | 128 ms                                                                | 118 ms: 1.09x faster                                  |
| tomli_loads          | 2.99 sec                                                              | 2.75 sec: 1.09x faster                                |
| pickle_dict          | 46.5 us                                                               | 44.6 us: 1.04x faster                                 |
| json_loads           | 36.6 us                                                               | 37.9 us: 1.04x slower                                 |
| unpickle             | 19.7 us                                                               | 20.8 us: 1.05x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 167 ms: 1.06x slower                                  |
| pickle_list          | 6.40 us                                                               | 6.95 us: 1.09x slower                                 |
| pickle               | 14.8 us                                                               | 16.5 us: 1.12x slower                                 |
| json_dumps           | 13.6 ms                                                               | 15.8 ms: 1.17x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (4): pickle_pure_python, unpickle_list, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 15.1 ms: 1.08x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 48.6 ms                                                               | 45.6 ms: 1.06x faster                                 |
| genshi_xml      | 73.6 ms                                                               | 69.6 ms: 1.06x faster                                 |
| genshi_text     | 31.9 ms                                                               | 33.6 ms: 1.05x slower                                 |
| mako            | 17.2 ms                                                               | 18.2 ms: 1.06x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.00x faster                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 621 ms: 1.51x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 637 ms: 1.49x faster                                  |
| async_tree_none            | 740 ms                                                                | 501 ms: 1.48x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 483 ms: 1.43x faster                                  |
| deepcopy                   | 503 us                                                                | 354 us: 1.42x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 823 ms: 1.38x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.32 sec: 1.37x faster                                |
| comprehensions             | 29.6 us                                                               | 22.0 us: 1.34x faster                                 |
| deepcopy_memo              | 57.5 us                                                               | 43.0 us: 1.34x faster                                 |
| unpack_sequence            | 68.5 ns                                                               | 51.6 ns: 1.33x faster                                 |
| async_tree_io              | 1.79 sec                                                              | 1.36 sec: 1.31x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 853 ms: 1.29x faster                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.07 ms: 1.23x faster                                 |
| deepcopy_reduce            | 4.45 us                                                               | 3.62 us: 1.23x faster                                 |
| raytrace                   | 418 ms                                                                | 340 ms: 1.23x faster                                  |
| logging_format             | 11.8 us                                                               | 9.82 us: 1.20x faster                                 |
| sympy_str                  | 425 ms                                                                | 358 ms: 1.19x faster                                  |
| sympy_integrate            | 31.4 ms                                                               | 27.0 ms: 1.16x faster                                 |
| go                         | 185 ms                                                                | 161 ms: 1.15x faster                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 85.8 ms: 1.15x faster                                 |
| sympy_expand               | 689 ms                                                                | 603 ms: 1.14x faster                                  |
| crypto_pyaes               | 112 ms                                                                | 98.5 ms: 1.13x faster                                 |
| chaos                      | 93.7 ms                                                               | 83.1 ms: 1.13x faster                                 |
| pycparser                  | 1.73 sec                                                              | 1.54 sec: 1.12x faster                                |
| regex_compile              | 197 ms                                                                | 175 ms: 1.12x faster                                  |
| thrift                     | 1.17 ms                                                               | 1.05 ms: 1.12x faster                                 |
| sqlglot_parse              | 1.89 ms                                                               | 1.69 ms: 1.12x faster                                 |
| unpickle_pure_python       | 319 us                                                                | 288 us: 1.11x faster                                  |
| deltablue                  | 5.05 ms                                                               | 4.57 ms: 1.11x faster                                 |
| sympy_sum                  | 229 ms                                                                | 207 ms: 1.11x faster                                  |
| float                      | 127 ms                                                                | 115 ms: 1.10x faster                                  |
| hexiom                     | 8.87 ms                                                               | 8.08 ms: 1.10x faster                                 |
| xml_etree_generate         | 128 ms                                                                | 118 ms: 1.09x faster                                  |
| tomli_loads                | 2.99 sec                                                              | 2.75 sec: 1.09x faster                                |
| html5lib                   | 95.8 ms                                                               | 88.4 ms: 1.08x faster                                 |
| spectral_norm              | 158 ms                                                                | 146 ms: 1.08x faster                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 6.12 sec: 1.08x faster                                |
| python_startup_no_site     | 16.3 ms                                                               | 15.1 ms: 1.08x faster                                 |
| nbody                      | 125 ms                                                                | 116 ms: 1.08x faster                                  |
| async_generators           | 617 ms                                                                | 575 ms: 1.07x faster                                  |
| pprint_pformat             | 2.03 sec                                                              | 1.89 sec: 1.07x faster                                |
| scimark_fft                | 499 ms                                                                | 467 ms: 1.07x faster                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 2.13 ms: 1.07x faster                                 |
| 2to3                       | 444 ms                                                                | 415 ms: 1.07x faster                                  |
| pathlib                    | 31.7 ms                                                               | 29.7 ms: 1.07x faster                                 |
| django_template            | 48.6 ms                                                               | 45.6 ms: 1.06x faster                                 |
| docutils                   | 4.06 sec                                                              | 3.82 sec: 1.06x faster                                |
| asyncio_tcp                | 958 ms                                                                | 901 ms: 1.06x faster                                  |
| genshi_xml                 | 73.6 ms                                                               | 69.6 ms: 1.06x faster                                 |
| sqlglot_normalize          | 148 ms                                                                | 140 ms: 1.06x faster                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 72.3 ms: 1.06x faster                                 |
| pprint_safe_repr           | 970 ms                                                                | 916 ms: 1.06x faster                                  |
| generators                 | 46.0 ms                                                               | 43.6 ms: 1.06x faster                                 |
| pickle_dict                | 46.5 us                                                               | 44.6 us: 1.04x faster                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.73 sec: 1.03x faster                                |
| json_loads                 | 36.6 us                                                               | 37.9 us: 1.04x slower                                 |
| mdp                        | 3.84 sec                                                              | 3.99 sec: 1.04x slower                                |
| regex_effbot               | 4.97 ms                                                               | 5.19 ms: 1.04x slower                                 |
| richards_super             | 67.9 ms                                                               | 71.4 ms: 1.05x slower                                 |
| unpickle                   | 19.7 us                                                               | 20.8 us: 1.05x slower                                 |
| genshi_text                | 31.9 ms                                                               | 33.6 ms: 1.05x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 167 ms: 1.06x slower                                  |
| mako                       | 17.2 ms                                                               | 18.2 ms: 1.06x slower                                 |
| coroutines                 | 30.1 ms                                                               | 32.0 ms: 1.06x slower                                 |
| pickle_list                | 6.40 us                                                               | 6.95 us: 1.09x slower                                 |
| coverage                   | 97.6 ms                                                               | 107 ms: 1.10x slower                                  |
| bench_mp_pool              | 18.4 ms                                                               | 20.4 ms: 1.11x slower                                 |
| pickle                     | 14.8 us                                                               | 16.5 us: 1.12x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 223 us: 1.12x slower                                  |
| regex_v8                   | 31.1 ms                                                               | 34.9 ms: 1.12x slower                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.35 ms: 1.16x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 15.8 ms: 1.17x slower                                 |
| telco                      | 9.71 ms                                                               | 11.3 ms: 1.17x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                          |

Benchmark hidden because not significant (24): tornado_http, logging_simple, pylint, pickle_pure_python, fannkuch, logging_silent, asyncio_websockets, scimark_sor, meteor_contest, scimark_lu, unpickle_list, gc_traversal, pidigits, regex_dna, xml_etree_process, xml_etree_parse, python_startup, pyflate, richards, sqlite_synth, json, bench_thread_pool, nqueens, dulwich_log
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.88x