# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.003x faster
- HPT reliability: 75.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 512 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 704 ms: 1.99x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 778 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 317 ms: 1.59x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 433 ms: 1.55x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.50x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 494 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 625 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 706 ms: 1.26x faster                                                   |
| async_generators           | 567 ms                                                       | 552 ms: 1.03x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 32.8 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.37x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| pidigits       | 251 ms                                                       | 229 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                       | 147 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                  |
| regex_dna      | 282 ms                                                       | 267 ms: 1.06x faster                                                   |
| regex_compile  | 182 ms                                                       | 191 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| pickle_pure_python   | 416 us                                                       | 438 us: 1.05x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 91.2 ms: 1.06x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 314 us: 1.08x slower                                                   |
| json_loads           | 34.3 us                                                      | 41.9 us: 1.22x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 34.6 ms: 1.54x slower                                                  |
| python_startup_no_site | 15.3 ms                                                      | 24.6 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 35.6 ms: 1.12x slower                                                  |
| django_template | 44.3 ms                                                      | 51.5 ms: 1.16x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 85.5 ms: 1.19x slower                                                  |
| mako            | 15.9 ms                                                      | 21.4 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 704 ms: 1.99x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 778 ms: 1.78x faster                                                   |
| mdp                        | 3.80 sec                                                     | 2.38 sec: 1.60x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 317 ms: 1.59x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.65 ms: 1.56x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 433 ms: 1.55x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.50x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 494 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 625 ms: 1.36x faster                                                   |
| deepcopy                   | 498 us                                                       | 368 us: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 706 ms: 1.26x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.52 us: 1.13x faster                                                  |
| spectral_norm              | 157 ms                                                       | 138 ms: 1.13x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| float                      | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.24 ms: 1.12x faster                                                  |
| scimark_sor                | 179 ms                                                       | 163 ms: 1.10x faster                                                   |
| pidigits                   | 251 ms                                                       | 229 ms: 1.09x faster                                                   |
| pylint                     | 470 ms                                                       | 435 ms: 1.08x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 47.0 us: 1.07x faster                                                  |
| go                         | 191 ms                                                       | 180 ms: 1.06x faster                                                   |
| regex_dna                  | 282 ms                                                       | 267 ms: 1.06x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.52 sec: 1.03x faster                                                 |
| async_generators           | 567 ms                                                       | 552 ms: 1.03x faster                                                   |
| pyflate                    | 664 ms                                                       | 686 ms: 1.03x slower                                                   |
| richards_super             | 73.2 ms                                                      | 75.7 ms: 1.03x slower                                                  |
| regex_compile              | 182 ms                                                       | 191 ms: 1.05x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.04 sec: 1.05x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 438 us: 1.05x slower                                                   |
| logging_silent             | 130 ns                                                       | 137 ns: 1.05x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 91.2 ms: 1.06x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 32.8 ms: 1.06x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.17 us: 1.07x slower                                                  |
| nqueens                    | 112 ms                                                       | 120 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.28 ms: 1.08x slower                                                  |
| telco                      | 12.2 ms                                                      | 13.1 ms: 1.08x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 314 us: 1.08x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 6.89 sec: 1.10x slower                                                 |
| fannkuch                   | 547 ms                                                       | 601 ms: 1.10x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.14 sec: 1.10x slower                                                 |
| richards                   | 65.5 ms                                                      | 72.3 ms: 1.10x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 112 ms: 1.11x slower                                                   |
| logging_format             | 9.24 us                                                      | 10.3 us: 1.11x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.8 ms: 1.12x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 34.0 ms: 1.12x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 35.6 ms: 1.12x slower                                                  |
| meteor_contest             | 150 ms                                                       | 170 ms: 1.14x slower                                                   |
| sympy_expand               | 601 ms                                                       | 682 ms: 1.14x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 239 ms: 1.14x slower                                                   |
| sympy_str                  | 379 ms                                                       | 433 ms: 1.14x slower                                                   |
| 2to3                       | 445 ms                                                       | 512 ms: 1.15x slower                                                   |
| json                       | 6.51 ms                                                      | 7.50 ms: 1.15x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.6 us: 1.15x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 169 ms: 1.15x slower                                                   |
| django_template            | 44.3 ms                                                      | 51.5 ms: 1.16x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.47 ms: 1.17x slower                                                  |
| raytrace                   | 344 ms                                                       | 404 ms: 1.17x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 85.5 ms: 1.19x slower                                                  |
| json_loads                 | 34.3 us                                                      | 41.9 us: 1.22x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 112 ms: 1.24x slower                                                   |
| nbody                      | 119 ms                                                       | 147 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 282 us: 1.25x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.63 ms: 1.26x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 5.82 ms: 1.31x slower                                                  |
| mako                       | 15.9 ms                                                      | 21.4 ms: 1.34x slower                                                  |
| coverage                   | 107 ms                                                       | 150 ms: 1.40x slower                                                   |
| python_startup             | 22.4 ms                                                      | 34.6 ms: 1.54x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 24.6 ms: 1.61x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 84.2 ms: 4.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (11): dulwich_log, asyncio_websockets, html5lib, deepcopy_reduce, regex_v8, docutils, tomli_loads, scimark_fft, pathlib, chaos, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 75.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x