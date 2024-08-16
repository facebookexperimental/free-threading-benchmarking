# Results vs. 3.12.0b1

- fork: python
- ref: 3.12
- machine: linux-x86_64
- commit hash: 9f153a2
- commit date: 2024-08-14
- overall geometric mean: 1.01x faster
- HPT reliability: 97.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.84x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|--------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| async_tree_io_tg   | 1.80 sec                                                              | 1.87 sec: 1.03x slower                               |
| async_tree_io      | 1.79 sec                                                              | 1.86 sec: 1.04x slower                               |
| async_tree_none_tg | 692 ms                                                                | 726 ms: 1.05x slower                                 |
| async_tree_none    | 740 ms                                                                | 820 ms: 1.11x slower                                 |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                         |

Benchmark hidden because not significant (9): async_tree_memoization_tg, asyncio_websockets, async_generators, async_tree_cpu_io_mixed, asyncio_tcp_ssl, coroutines, async_tree_cpu_io_mixed_tg, async_tree_memoization, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| nbody          | 125 ms                                                                | 117 ms: 1.07x faster                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                         |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 268 ms: 1.07x faster                                 |
| regex_compile  | 197 ms                                                                | 186 ms: 1.06x faster                                 |
| regex_v8       | 31.1 ms                                                               | 29.9 ms: 1.04x faster                                |
| Geometric mean | (ref)                                                                 | 1.04x faster                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|---------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| unpickle_list       | 7.19 us                                                               | 6.83 us: 1.05x faster                                |
| tomli_loads         | 2.99 sec                                                              | 2.86 sec: 1.04x faster                               |
| xml_etree_parse     | 230 ms                                                                | 244 ms: 1.06x slower                                 |
| pickle              | 14.8 us                                                               | 15.9 us: 1.07x slower                                |
| xml_etree_generate  | 128 ms                                                                | 138 ms: 1.07x slower                                 |
| pickle_list         | 6.40 us                                                               | 7.01 us: 1.09x slower                                |
| unpickle            | 19.7 us                                                               | 21.6 us: 1.10x slower                                |
| xml_etree_iterparse | 157 ms                                                                | 173 ms: 1.10x slower                                 |
| Geometric mean      | (ref)                                                                 | 1.02x slower                                         |

Benchmark hidden because not significant (6): unpickle_pure_python, xml_etree_process, pickle_pure_python, pickle_dict, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| python_startup | 21.2 ms                                                               | 22.7 ms: 1.07x slower                                |
| Geometric mean | (ref)                                                                 | 1.03x slower                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| django_template | 48.6 ms                                                               | 45.4 ms: 1.07x faster                                |
| mako            | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                |
| genshi_xml      | 73.6 ms                                                               | 69.1 ms: 1.07x faster                                |
| genshi_text     | 31.9 ms                                                               | 30.3 ms: 1.05x faster                                |
| Geometric mean  | (ref)                                                                 | 1.06x faster                                         |

All benchmarks:
===============

| Benchmark                | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|--------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| mypy2                    | 1.28 sec                                                              | 1.02 sec: 1.26x faster                               |
| logging_format           | 11.8 us                                                               | 9.56 us: 1.24x faster                                |
| sympy_expand             | 689 ms                                                                | 591 ms: 1.17x faster                                 |
| spectral_norm            | 158 ms                                                                | 136 ms: 1.16x faster                                 |
| deltablue                | 5.05 ms                                                               | 4.45 ms: 1.13x faster                                |
| deepcopy_memo            | 57.5 us                                                               | 51.0 us: 1.13x faster                                |
| sympy_str                | 425 ms                                                                | 379 ms: 1.12x faster                                 |
| dulwich_log              | 114 ms                                                                | 104 ms: 1.10x faster                                 |
| hexiom                   | 8.87 ms                                                               | 8.19 ms: 1.08x faster                                |
| sympy_integrate          | 31.4 ms                                                               | 29.0 ms: 1.08x faster                                |
| scimark_sparse_mat_mult  | 7.47 ms                                                               | 6.94 ms: 1.08x faster                                |
| django_template          | 48.6 ms                                                               | 45.4 ms: 1.07x faster                                |
| regex_dna                | 287 ms                                                                | 268 ms: 1.07x faster                                 |
| nbody                    | 125 ms                                                                | 117 ms: 1.07x faster                                 |
| go                       | 185 ms                                                                | 173 ms: 1.07x faster                                 |
| mako                     | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                |
| deepcopy_reduce          | 4.45 us                                                               | 4.18 us: 1.07x faster                                |
| genshi_xml               | 73.6 ms                                                               | 69.1 ms: 1.07x faster                                |
| thrift                   | 1.17 ms                                                               | 1.10 ms: 1.06x faster                                |
| regex_compile            | 197 ms                                                                | 186 ms: 1.06x faster                                 |
| unpickle_list            | 7.19 us                                                               | 6.83 us: 1.05x faster                                |
| genshi_text              | 31.9 ms                                                               | 30.3 ms: 1.05x faster                                |
| sympy_sum                | 229 ms                                                                | 218 ms: 1.05x faster                                 |
| fannkuch                 | 551 ms                                                                | 525 ms: 1.05x faster                                 |
| tomli_loads              | 2.99 sec                                                              | 2.86 sec: 1.04x faster                               |
| regex_v8                 | 31.1 ms                                                               | 29.9 ms: 1.04x faster                                |
| scimark_fft              | 499 ms                                                                | 481 ms: 1.04x faster                                 |
| pycparser                | 1.73 sec                                                              | 1.68 sec: 1.03x faster                               |
| async_tree_io_tg         | 1.80 sec                                                              | 1.87 sec: 1.03x slower                               |
| async_tree_io            | 1.79 sec                                                              | 1.86 sec: 1.04x slower                               |
| async_tree_none_tg       | 692 ms                                                                | 726 ms: 1.05x slower                                 |
| nqueens                  | 110 ms                                                                | 116 ms: 1.05x slower                                 |
| xml_etree_parse          | 230 ms                                                                | 244 ms: 1.06x slower                                 |
| python_startup           | 21.2 ms                                                               | 22.7 ms: 1.07x slower                                |
| aiohttp                  | 1.92 ms                                                               | 2.05 ms: 1.07x slower                                |
| json                     | 6.68 ms                                                               | 7.14 ms: 1.07x slower                                |
| pickle                   | 14.8 us                                                               | 15.9 us: 1.07x slower                                |
| xml_etree_generate       | 128 ms                                                                | 138 ms: 1.07x slower                                 |
| pickle_list              | 6.40 us                                                               | 7.01 us: 1.09x slower                                |
| unpickle                 | 19.7 us                                                               | 21.6 us: 1.10x slower                                |
| xml_etree_iterparse      | 157 ms                                                                | 173 ms: 1.10x slower                                 |
| bench_thread_pool        | 3.11 ms                                                               | 3.42 ms: 1.10x slower                                |
| async_tree_none          | 740 ms                                                                | 820 ms: 1.11x slower                                 |
| typing_runtime_protocols | 199 us                                                                | 224 us: 1.12x slower                                 |
| gc_traversal             | 5.61 ms                                                               | 6.42 ms: 1.14x slower                                |
| bench_mp_pool            | 18.4 ms                                                               | 21.2 ms: 1.16x slower                                |
| Geometric mean           | (ref)                                                                 | 1.01x faster                                         |

Benchmark hidden because not significant (59): unpickle_pure_python, pylint, xml_etree_process, deepcopy, raytrace, sqlglot_normalize, comprehensions, generators, gunicorn, pickle_pure_python, async_tree_memoization_tg, sqlalchemy_declarative, pickle_dict, logging_simple, sqlglot_parse, pprint_pformat, crypto_pyaes, mdp, telco, float, json_loads, scimark_monte_carlo, asyncio_websockets, meteor_contest, chaos, create_gc_cycles, richards, dask, coverage, scimark_sor, tornado_http, pathlib, async_generators, docutils, python_startup_no_site, scimark_lu, pprint_safe_repr, pyflate, sqlite_synth, async_tree_cpu_io_mixed, pidigits, asyncio_tcp_ssl, regex_effbot, sqlalchemy_imperative, coroutines, sqlglot_transpile, async_tree_cpu_io_mixed_tg, bpe_tokeniser, richards_super, async_tree_memoization, 2to3, logging_silent, asyncio_tcp, json_dumps, unpack_sequence, flaskblogging, chameleon, html5lib, sqlglot_optimize

# HPT report

- Reliability score: 97.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.84x