# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.038x faster
- HPT reliability: 51.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 512 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 704 ms: 2.75x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 778 ms: 2.37x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 317 ms: 2.22x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 433 ms: 2.15x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 494 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 625 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 706 ms: 1.53x faster                                                   |
| async_generators           | 589 ms                                                 | 552 ms: 1.07x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.8 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.69x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| pidigits       | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                 | 147 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                  |
| regex_dna      | 278 ms                                                 | 267 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 314 us: 1.05x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 91.2 ms: 1.09x slower                                                  |
| json_loads           | 37.9 us                                                | 41.9 us: 1.11x slower                                                  |
| json_dumps           | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (3): tomli_loads, pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 24.6 ms: 1.40x slower                                                  |
| python_startup         | 23.7 ms                                                | 34.6 ms: 1.46x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 51.5 ms: 1.15x slower                                                  |
| genshi_text     | 30.2 ms                                                | 35.6 ms: 1.18x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 85.5 ms: 1.27x slower                                                  |
| mako            | 15.7 ms                                                | 21.4 ms: 1.36x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 704 ms: 2.75x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 778 ms: 2.37x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 317 ms: 2.22x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 433 ms: 2.15x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 494 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 625 ms: 1.76x faster                                                   |
| mdp                        | 3.97 sec                                               | 2.38 sec: 1.67x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 3.65 ms: 1.61x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 706 ms: 1.53x faster                                                   |
| deepcopy                   | 468 us                                                 | 368 us: 1.27x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                  |
| float                      | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.52 sec: 1.18x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| spectral_norm              | 156 ms                                                 | 138 ms: 1.12x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 47.0 us: 1.12x faster                                                  |
| dulwich_log                | 100 ms                                                 | 90.5 ms: 1.11x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.52 us: 1.10x faster                                                  |
| pidigits                   | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| pylint                     | 465 ms                                                 | 435 ms: 1.07x faster                                                   |
| async_generators           | 589 ms                                                 | 552 ms: 1.07x faster                                                   |
| pyflate                    | 727 ms                                                 | 686 ms: 1.06x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.6 us: 1.06x faster                                                  |
| regex_dna                  | 278 ms                                                 | 267 ms: 1.04x faster                                                   |
| scimark_fft                | 500 ms                                                 | 481 ms: 1.04x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 112 ms: 1.04x slower                                                   |
| richards_super             | 72.8 ms                                                | 75.7 ms: 1.04x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.89 sec: 1.05x slower                                                 |
| go                         | 172 ms                                                 | 180 ms: 1.05x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 314 us: 1.05x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.04 sec: 1.07x slower                                                 |
| logging_format             | 9.59 us                                                | 10.3 us: 1.07x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 239 ms: 1.08x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.14 sec: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.28 ms: 1.09x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 91.2 ms: 1.09x slower                                                  |
| generators                 | 41.1 ms                                                | 44.8 ms: 1.09x slower                                                  |
| json                       | 6.85 ms                                                | 7.50 ms: 1.10x slower                                                  |
| json_loads                 | 37.9 us                                                | 41.9 us: 1.11x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 169 ms: 1.11x slower                                                   |
| fannkuch                   | 540 ms                                                 | 601 ms: 1.11x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.8 ms: 1.11x slower                                                  |
| 2to3                       | 456 ms                                                 | 512 ms: 1.12x slower                                                   |
| sympy_str                  | 385 ms                                                 | 433 ms: 1.12x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.0 ms: 1.14x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.47 ms: 1.14x slower                                                  |
| django_template            | 44.9 ms                                                | 51.5 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 112 ms: 1.16x slower                                                   |
| meteor_contest             | 146 ms                                                 | 170 ms: 1.16x slower                                                   |
| sympy_expand               | 582 ms                                                 | 682 ms: 1.17x slower                                                   |
| genshi_text                | 30.2 ms                                                | 35.6 ms: 1.18x slower                                                  |
| richards                   | 60.3 ms                                                | 72.3 ms: 1.20x slower                                                  |
| nbody                      | 119 ms                                                 | 147 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 282 us: 1.26x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 85.5 ms: 1.27x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.54 ms: 1.31x slower                                                  |
| mako                       | 15.7 ms                                                | 21.4 ms: 1.36x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.82 ms: 1.36x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 33.8 ms: 1.37x slower                                                  |
| telco                      | 9.59 ms                                                | 13.1 ms: 1.37x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 24.6 ms: 1.40x slower                                                  |
| python_startup             | 23.7 ms                                                | 34.6 ms: 1.46x slower                                                  |
| coverage                   | 95.4 ms                                                | 150 ms: 1.58x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 84.2 ms: 4.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (18): pathlib, logging_simple, scimark_sor, tomli_loads, logging_silent, raytrace, asyncio_websockets, docutils, regex_v8, deepcopy_reduce, pickle_pure_python, html5lib, chaos, regex_compile, sqlalchemy_declarative, nqueens, xml_etree_generate, bench_thread_pool
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 51.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x