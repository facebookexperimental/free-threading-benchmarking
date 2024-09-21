# Results vs. 3.12.6

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 53.51%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 4.22 sec: 1.06x slower                                                |
| html5lib       | 88.9 ms                                                | 94.5 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 647 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.33 sec: 1.46x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 643 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 494 ms: 1.43x faster                                                  |
| async_tree_none            | 741 ms                                                 | 523 ms: 1.42x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.42 sec: 1.30x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 875 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 893 ms: 1.21x faster                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.90 sec: 1.03x slower                                                |
| asyncio_websockets         | 748 ms                                                 | 781 ms: 1.04x slower                                                  |
| asyncio_tcp                | 923 ms                                                 | 972 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                          |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 310 ms: 1.11x slower                                                  |
| regex_v8       | 32.5 ms                                                | 36.2 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict         | 52.7 us                                                | 45.7 us: 1.15x faster                                                 |
| tomli_loads         | 2.88 sec                                               | 2.72 sec: 1.06x faster                                                |
| pickle_list         | 6.97 us                                                | 7.25 us: 1.04x slower                                                 |
| unpickle_list       | 6.83 us                                                | 7.18 us: 1.05x slower                                                 |
| xml_etree_iterparse | 169 ms                                                 | 182 ms: 1.07x slower                                                  |
| json_dumps          | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (8): pickle, pickle_pure_python, unpickle, unpickle_pure_python, json_loads, xml_etree_generate, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 26.1 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                | 72.3 ms: 1.07x slower                                                 |
| mako           | 15.7 ms                                                | 18.5 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 647 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.33 sec: 1.46x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 643 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 494 ms: 1.43x faster                                                  |
| async_tree_none            | 741 ms                                                 | 523 ms: 1.42x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 39.5 us: 1.33x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.42 sec: 1.30x faster                                                |
| deepcopy                   | 468 us                                                 | 362 us: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 875 ms: 1.26x faster                                                  |
| comprehensions             | 27.1 us                                                | 22.1 us: 1.23x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 893 ms: 1.21x faster                                                  |
| pickle_dict                | 52.7 us                                                | 45.7 us: 1.15x faster                                                 |
| raytrace                   | 408 ms                                                 | 358 ms: 1.14x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 95.7 ms: 1.12x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.60 us: 1.10x faster                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.13 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 89.4 ms: 1.08x faster                                                 |
| scimark_fft                | 500 ms                                                 | 470 ms: 1.06x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.72 sec: 1.06x faster                                                |
| bpe_tokeniser              | 6.59 sec                                               | 6.41 sec: 1.03x faster                                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.90 sec: 1.03x slower                                                |
| pprint_safe_repr           | 967 ms                                                 | 1.00 sec: 1.03x slower                                                |
| pickle_list                | 6.97 us                                                | 7.25 us: 1.04x slower                                                 |
| asyncio_websockets         | 748 ms                                                 | 781 ms: 1.04x slower                                                  |
| json                       | 6.85 ms                                                | 7.18 ms: 1.05x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.18 us: 1.05x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 972 ms: 1.05x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 6.19 ms: 1.06x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.22 sec: 1.06x slower                                                |
| html5lib                   | 88.9 ms                                                | 94.5 ms: 1.06x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 72.3 ms: 1.07x slower                                                 |
| dulwich_log                | 100 ms                                                 | 108 ms: 1.07x slower                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 182 ms: 1.07x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                 |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                  |
| sympy_expand               | 582 ms                                                 | 635 ms: 1.09x slower                                                  |
| richards                   | 60.3 ms                                                | 66.0 ms: 1.09x slower                                                 |
| python_startup             | 23.7 ms                                                | 26.1 ms: 1.10x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.17 ms: 1.10x slower                                                 |
| hexiom                     | 8.27 ms                                                | 9.21 ms: 1.11x slower                                                 |
| regex_dna                  | 278 ms                                                 | 310 ms: 1.11x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 36.2 ms: 1.11x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.89 ms: 1.12x slower                                                 |
| deltablue                  | 4.27 ms                                                | 4.79 ms: 1.12x slower                                                 |
| mako                       | 15.7 ms                                                | 18.5 ms: 1.18x slower                                                 |
| telco                      | 9.59 ms                                                | 11.5 ms: 1.20x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 72.4 ns: 1.20x slower                                                 |
| coverage                   | 95.4 ms                                                | 121 ms: 1.27x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 26.6 ms: 1.29x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.70 ms: 1.39x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (47): pickle, sympy_sum, pickle_pure_python, pathlib, sqlglot_normalize, unpickle, nqueens, richards_super, sqlglot_transpile, scimark_lu, go, chaos, 2to3, tornado_http, mdp, unpickle_pure_python, json_loads, pycparser, generators, sympy_integrate, async_generators, pprint_pformat, xml_etree_generate, python_startup_no_site, sqlglot_optimize, logging_format, regex_effbot, pyflate, coroutines, regex_compile, deepcopy_reduce, pidigits, float, typing_runtime_protocols, logging_silent, genshi_text, spectral_norm, scimark_sor, xml_etree_process, sqlite_synth, django_template, meteor_contest, sympy_str, sqlglot_parse, fannkuch, xml_etree_parse, pylint
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 53.51% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x