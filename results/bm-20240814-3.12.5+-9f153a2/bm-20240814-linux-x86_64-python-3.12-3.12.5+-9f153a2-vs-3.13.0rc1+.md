# Results vs. 3.13.0rc1+

- fork: python
- ref: 3.12
- machine: linux-x86_64
- commit hash: 9f153a2
- commit date: 2024-08-14
- overall geometric mean: 1.03x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| async_generators           | 592 ms                                                  | 615 ms: 1.04x slower                                 |
| coroutines                 | 29.2 ms                                                 | 30.6 ms: 1.05x slower                                |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 1.14 sec: 1.27x slower                               |
| async_tree_io_tg           | 1.46 sec                                                | 1.87 sec: 1.28x slower                               |
| async_tree_memoization     | 745 ms                                                  | 975 ms: 1.31x slower                                 |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.12 sec: 1.32x slower                               |
| async_tree_io              | 1.38 sec                                                | 1.86 sec: 1.35x slower                               |
| async_tree_memoization_tg  | 672 ms                                                  | 912 ms: 1.36x slower                                 |
| async_tree_none_tg         | 521 ms                                                  | 726 ms: 1.39x slower                                 |
| async_tree_none            | 576 ms                                                  | 820 ms: 1.42x slower                                 |
| Geometric mean             | (ref)                                                   | 1.20x slower                                         |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| nbody          | 124 ms                                                  | 117 ms: 1.06x faster                                 |
| pidigits       | 248 ms                                                  | 256 ms: 1.04x slower                                 |
| float          | 115 ms                                                  | 124 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                   | 1.02x slower                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 29.9 ms: 1.08x faster                                |
| regex_dna      | 288 ms                                                  | 268 ms: 1.07x faster                                 |
| regex_effbot   | 4.84 ms                                                 | 5.02 ms: 1.04x slower                                |
| regex_compile  | 177 ms                                                  | 186 ms: 1.05x slower                                 |
| Geometric mean | (ref)                                                   | 1.02x faster                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|--------------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| json_dumps         | 14.9 ms                                                 | 14.0 ms: 1.06x faster                                |
| tomli_loads        | 2.80 sec                                                | 2.86 sec: 1.02x slower                               |
| pickle_pure_python | 417 us                                                  | 436 us: 1.05x slower                                 |
| xml_etree_generate | 129 ms                                                  | 138 ms: 1.07x slower                                 |
| Geometric mean     | (ref)                                                   | 1.01x slower                                         |

Benchmark hidden because not significant (10): xml_etree_process, pickle_dict, xml_etree_iterparse, json_loads, unpickle, unpickle_list, unpickle_pure_python, pickle_list, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|------------------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 16.2 ms: 1.11x slower                                |
| Geometric mean         | (ref)                                                   | 1.07x slower                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_text, django_template, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 |
|----------------------------|:-------------------------------------------------------:|:----------------------------------------------------:|
| flaskblogging              | 8.78 ms                                                 | 6.97 ms: 1.26x faster                                |
| create_gc_cycles           | 2.46 ms                                                 | 2.00 ms: 1.23x faster                                |
| telco                      | 11.4 ms                                                 | 9.53 ms: 1.20x faster                                |
| gunicorn                   | 2.25 ms                                                 | 1.92 ms: 1.17x faster                                |
| spectral_norm              | 159 ms                                                  | 136 ms: 1.17x faster                                 |
| coverage                   | 110 ms                                                  | 96.9 ms: 1.14x faster                                |
| go                         | 195 ms                                                  | 173 ms: 1.13x faster                                 |
| richards_super             | 76.3 ms                                                 | 69.7 ms: 1.10x faster                                |
| aiohttp                    | 2.23 ms                                                 | 2.05 ms: 1.09x faster                                |
| regex_v8                   | 32.4 ms                                                 | 29.9 ms: 1.08x faster                                |
| sqlite_synth               | 4.07 us                                                 | 3.77 us: 1.08x faster                                |
| meteor_contest             | 157 ms                                                  | 146 ms: 1.07x faster                                 |
| regex_dna                  | 288 ms                                                  | 268 ms: 1.07x faster                                 |
| sympy_expand               | 631 ms                                                  | 591 ms: 1.07x faster                                 |
| json_dumps                 | 14.9 ms                                                 | 14.0 ms: 1.06x faster                                |
| nbody                      | 124 ms                                                  | 117 ms: 1.06x faster                                 |
| richards                   | 65.8 ms                                                 | 62.8 ms: 1.05x faster                                |
| fannkuch                   | 543 ms                                                  | 525 ms: 1.03x faster                                 |
| tomli_loads                | 2.80 sec                                                | 2.86 sec: 1.02x slower                               |
| pidigits                   | 248 ms                                                  | 256 ms: 1.04x slower                                 |
| regex_effbot               | 4.84 ms                                                 | 5.02 ms: 1.04x slower                                |
| async_generators           | 592 ms                                                  | 615 ms: 1.04x slower                                 |
| pickle_pure_python         | 417 us                                                  | 436 us: 1.05x slower                                 |
| coroutines                 | 29.2 ms                                                 | 30.6 ms: 1.05x slower                                |
| regex_compile              | 177 ms                                                  | 186 ms: 1.05x slower                                 |
| dask                       | 872 ms                                                  | 916 ms: 1.05x slower                                 |
| xml_etree_generate         | 129 ms                                                  | 138 ms: 1.07x slower                                 |
| pycparser                  | 1.57 sec                                                | 1.68 sec: 1.07x slower                               |
| nqueens                    | 108 ms                                                  | 116 ms: 1.07x slower                                 |
| logging_silent             | 130 ns                                                  | 139 ns: 1.07x slower                                 |
| scimark_monte_carlo        | 89.9 ms                                                 | 96.8 ms: 1.08x slower                                |
| logging_simple             | 8.98 us                                                 | 9.68 us: 1.08x slower                                |
| pathlib                    | 29.3 ms                                                 | 31.6 ms: 1.08x slower                                |
| bpe_tokeniser              | 6.25 sec                                                | 6.76 sec: 1.08x slower                               |
| float                      | 115 ms                                                  | 124 ms: 1.08x slower                                 |
| gc_traversal               | 5.91 ms                                                 | 6.42 ms: 1.09x slower                                |
| chaos                      | 84.7 ms                                                 | 92.1 ms: 1.09x slower                                |
| json                       | 6.55 ms                                                 | 7.14 ms: 1.09x slower                                |
| bench_mp_pool              | 19.4 ms                                                 | 21.2 ms: 1.10x slower                                |
| crypto_pyaes               | 99.8 ms                                                 | 110 ms: 1.10x slower                                 |
| python_startup_no_site     | 14.6 ms                                                 | 16.2 ms: 1.11x slower                                |
| bench_thread_pool          | 3.06 ms                                                 | 3.42 ms: 1.12x slower                                |
| generators                 | 39.2 ms                                                 | 44.7 ms: 1.14x slower                                |
| raytrace                   | 350 ms                                                  | 405 ms: 1.16x slower                                 |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 1.14 sec: 1.27x slower                               |
| async_tree_io_tg           | 1.46 sec                                                | 1.87 sec: 1.28x slower                               |
| async_tree_memoization     | 745 ms                                                  | 975 ms: 1.31x slower                                 |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.12 sec: 1.32x slower                               |
| async_tree_io              | 1.38 sec                                                | 1.86 sec: 1.35x slower                               |
| async_tree_memoization_tg  | 672 ms                                                  | 912 ms: 1.36x slower                                 |
| comprehensions             | 20.9 us                                                 | 28.6 us: 1.37x slower                                |
| async_tree_none_tg         | 521 ms                                                  | 726 ms: 1.39x slower                                 |
| async_tree_none            | 576 ms                                                  | 820 ms: 1.42x slower                                 |
| Geometric mean             | (ref)                                                   | 1.03x slower                                         |

Benchmark hidden because not significant (49): genshi_text, xml_etree_process, unpack_sequence, django_template, asyncio_websockets, deltablue, sympy_integrate, pickle_dict, deepcopy_reduce, xml_etree_iterparse, hexiom, chameleon, sqlglot_normalize, deepcopy_memo, scimark_sor, thrift, mdp, scimark_sparse_mat_mult, json_loads, pprint_pformat, asyncio_tcp, pyflate, deepcopy, mako, scimark_lu, logging_format, sqlglot_transpile, asyncio_tcp_ssl, scimark_fft, docutils, genshi_xml, unpickle, pprint_safe_repr, pylint, html5lib, sympy_sum, unpickle_list, unpickle_pure_python, pickle_list, python_startup, sqlglot_parse, sympy_str, xml_etree_parse, pickle, 2to3, typing_runtime_protocols, dulwich_log, sqlglot_optimize, tornado_http
Ignored benchmarks (3) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x