# Results vs. 3.13.0b1

- fork: python
- ref: 3.12
- machine: linux-x86_64
- commit hash: 9f153a2
- commit date: 2024-08-14
- overall geometric mean: 1.00x faster
- HPT reliability: 96.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| docutils       | 3.94 sec                                                              | 4.05 sec: 1.03x slower                               |
| html5lib       | 92.0 ms                                                               | 100 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                                 | 1.04x slower                                         |

Benchmark hidden because not significant (3): 2to3, chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| asyncio_websockets         | 728 ms                                                                | 752 ms: 1.03x slower                                 |
| coroutines                 | 29.3 ms                                                               | 30.6 ms: 1.04x slower                                |
| async_generators           | 588 ms                                                                | 615 ms: 1.05x slower                                 |
| async_tree_memoization     | 775 ms                                                                | 975 ms: 1.26x slower                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 1.14 sec: 1.27x slower                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.12 sec: 1.28x slower                               |
| async_tree_io_tg           | 1.43 sec                                                              | 1.87 sec: 1.30x slower                               |
| async_tree_memoization_tg  | 692 ms                                                                | 912 ms: 1.32x slower                                 |
| async_tree_io              | 1.39 sec                                                              | 1.86 sec: 1.34x slower                               |
| async_tree_none_tg         | 526 ms                                                                | 726 ms: 1.38x slower                                 |
| async_tree_none            | 523 ms                                                                | 820 ms: 1.57x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.21x slower                                         |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| nbody          | 126 ms                                                                | 117 ms: 1.08x faster                                 |
| float          | 115 ms                                                                | 124 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                                 | 1.00x slower                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 29.9 ms: 1.24x faster                                |
| regex_dna      | 284 ms                                                                | 268 ms: 1.06x faster                                 |
| regex_effbot   | 4.63 ms                                                               | 5.02 ms: 1.08x slower                                |
| Geometric mean | (ref)                                                                 | 1.05x faster                                         |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 7.01 us: 1.07x faster                                |
| json_loads           | 37.9 us                                                               | 35.9 us: 1.05x faster                                |
| pickle               | 15.2 us                                                               | 15.9 us: 1.04x slower                                |
| xml_etree_iterparse  | 163 ms                                                                | 173 ms: 1.06x slower                                 |
| unpickle_pure_python | 285 us                                                                | 304 us: 1.06x slower                                 |
| xml_etree_parse      | 216 ms                                                                | 244 ms: 1.13x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 138 ms: 1.15x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                         |

Benchmark hidden because not significant (7): unpickle, pickle_dict, xml_etree_process, json_dumps, unpickle_list, tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| python_startup | 23.5 ms                                                               | 22.7 ms: 1.04x faster                                |
| Geometric mean | (ref)                                                                 | 1.01x faster                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_text, genshi_xml, mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------:|
| telco                      | 229 ms                                                                | 9.53 ms: 24.03x faster                               |
| create_gc_cycles           | 2.49 ms                                                               | 2.00 ms: 1.24x faster                                |
| coverage                   | 121 ms                                                                | 96.9 ms: 1.24x faster                                |
| regex_v8                   | 37.1 ms                                                               | 29.9 ms: 1.24x faster                                |
| flaskblogging              | 8.08 ms                                                               | 6.97 ms: 1.16x faster                                |
| go                         | 193 ms                                                                | 173 ms: 1.12x faster                                 |
| spectral_norm              | 151 ms                                                                | 136 ms: 1.11x faster                                 |
| richards                   | 68.8 ms                                                               | 62.8 ms: 1.10x faster                                |
| aiohttp                    | 2.24 ms                                                               | 2.05 ms: 1.09x faster                                |
| sympy_expand               | 638 ms                                                                | 591 ms: 1.08x faster                                 |
| nbody                      | 126 ms                                                                | 117 ms: 1.08x faster                                 |
| pyflate                    | 710 ms                                                                | 664 ms: 1.07x faster                                 |
| meteor_contest             | 156 ms                                                                | 146 ms: 1.07x faster                                 |
| pickle_list                | 7.48 us                                                               | 7.01 us: 1.07x faster                                |
| mdp                        | 4.01 sec                                                              | 3.77 sec: 1.06x faster                               |
| regex_dna                  | 284 ms                                                                | 268 ms: 1.06x faster                                 |
| json_loads                 | 37.9 us                                                               | 35.9 us: 1.05x faster                                |
| richards_super             | 73.5 ms                                                               | 69.7 ms: 1.05x faster                                |
| sqlglot_normalize          | 150 ms                                                                | 144 ms: 1.05x faster                                 |
| sqlite_synth               | 3.94 us                                                               | 3.77 us: 1.04x faster                                |
| python_startup             | 23.5 ms                                                               | 22.7 ms: 1.04x faster                                |
| docutils                   | 3.94 sec                                                              | 4.05 sec: 1.03x slower                               |
| asyncio_websockets         | 728 ms                                                                | 752 ms: 1.03x slower                                 |
| bpe_tokeniser              | 6.53 sec                                                              | 6.76 sec: 1.03x slower                               |
| scimark_lu                 | 150 ms                                                                | 155 ms: 1.04x slower                                 |
| pickle                     | 15.2 us                                                               | 15.9 us: 1.04x slower                                |
| coroutines                 | 29.3 ms                                                               | 30.6 ms: 1.04x slower                                |
| async_generators           | 588 ms                                                                | 615 ms: 1.05x slower                                 |
| json                       | 6.79 ms                                                               | 7.14 ms: 1.05x slower                                |
| xml_etree_iterparse        | 163 ms                                                                | 173 ms: 1.06x slower                                 |
| unpickle_pure_python       | 285 us                                                                | 304 us: 1.06x slower                                 |
| dulwich_log                | 97.5 ms                                                               | 104 ms: 1.07x slower                                 |
| nqueens                    | 108 ms                                                                | 116 ms: 1.07x slower                                 |
| dask                       | 856 ms                                                                | 916 ms: 1.07x slower                                 |
| crypto_pyaes               | 102 ms                                                                | 110 ms: 1.08x slower                                 |
| bench_mp_pool              | 19.7 ms                                                               | 21.2 ms: 1.08x slower                                |
| float                      | 115 ms                                                                | 124 ms: 1.08x slower                                 |
| regex_effbot               | 4.63 ms                                                               | 5.02 ms: 1.08x slower                                |
| html5lib                   | 92.0 ms                                                               | 100 ms: 1.09x slower                                 |
| scimark_monte_carlo        | 89.0 ms                                                               | 96.8 ms: 1.09x slower                                |
| generators                 | 40.7 ms                                                               | 44.7 ms: 1.10x slower                                |
| gc_traversal               | 5.80 ms                                                               | 6.42 ms: 1.11x slower                                |
| xml_etree_parse            | 216 ms                                                                | 244 ms: 1.13x slower                                 |
| chaos                      | 81.5 ms                                                               | 92.1 ms: 1.13x slower                                |
| bench_thread_pool          | 3.01 ms                                                               | 3.42 ms: 1.14x slower                                |
| xml_etree_generate         | 120 ms                                                                | 138 ms: 1.15x slower                                 |
| raytrace                   | 351 ms                                                                | 405 ms: 1.15x slower                                 |
| async_tree_memoization     | 775 ms                                                                | 975 ms: 1.26x slower                                 |
| comprehensions             | 22.6 us                                                               | 28.6 us: 1.26x slower                                |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 1.14 sec: 1.27x slower                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 1.12 sec: 1.28x slower                               |
| unpack_sequence            | 54.6 ns                                                               | 70.8 ns: 1.30x slower                                |
| async_tree_io_tg           | 1.43 sec                                                              | 1.87 sec: 1.30x slower                               |
| async_tree_memoization_tg  | 692 ms                                                                | 912 ms: 1.32x slower                                 |
| async_tree_io              | 1.39 sec                                                              | 1.86 sec: 1.34x slower                               |
| async_tree_none_tg         | 526 ms                                                                | 726 ms: 1.38x slower                                 |
| async_tree_none            | 523 ms                                                                | 820 ms: 1.57x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                         |

Benchmark hidden because not significant (45): genshi_text, genshi_xml, sympy_sum, scimark_sor, sqlglot_parse, mako, deepcopy_reduce, hexiom, unpickle, pprint_pformat, deepcopy, deltablue, pickle_dict, fannkuch, pycparser, pprint_safe_repr, regex_compile, django_template, pathlib, asyncio_tcp_ssl, pidigits, deepcopy_memo, xml_etree_process, json_dumps, sympy_str, unpickle_list, sympy_integrate, chameleon, tomli_loads, typing_runtime_protocols, python_startup_no_site, scimark_sparse_mat_mult, thrift, asyncio_tcp, gunicorn, logging_silent, pickle_pure_python, logging_format, scimark_fft, sqlglot_optimize, pylint, tornado_http, sqlglot_transpile, 2to3, logging_simple
Ignored benchmarks (3) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 96.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x