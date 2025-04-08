# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.033x faster
- HPT reliability: 76.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 511 ms: 1.12x slower                                                  |
| html5lib       | 88.9 ms                                                | 99.3 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 703 ms: 2.75x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 793 ms: 2.33x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 316 ms: 2.23x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 451 ms: 2.06x faster                                                  |
| async_tree_none            | 741 ms                                                 | 368 ms: 2.02x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 495 ms: 1.97x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 617 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 650 ms: 1.66x faster                                                  |
| async_generators           | 589 ms                                                 | 559 ms: 1.05x faster                                                  |
| coroutines                 | 29.5 ms                                                | 36.6 ms: 1.24x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.68x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 100 ms: 1.23x faster                                                  |
| pidigits       | 250 ms                                                 | 231 ms: 1.08x faster                                                  |
| nbody          | 119 ms                                                 | 150 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                 |
| regex_dna      | 278 ms                                                 | 289 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 143 ms: 1.18x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 216 ms: 1.12x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 312 us: 1.04x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 91.5 ms: 1.09x slower                                                 |
| json_loads           | 37.9 us                                                | 41.7 us: 1.10x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 497 us: 1.14x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.8 ms: 1.24x slower                                                 |
| python_startup         | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 79.3 ms: 1.17x slower                                                 |
| django_template | 44.9 ms                                                | 53.0 ms: 1.18x slower                                                 |
| genshi_text     | 30.2 ms                                                | 37.0 ms: 1.23x slower                                                 |
| mako            | 15.7 ms                                                | 21.4 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 703 ms: 2.75x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 793 ms: 2.33x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 316 ms: 2.23x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 451 ms: 2.06x faster                                                  |
| async_tree_none            | 741 ms                                                 | 368 ms: 2.02x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 495 ms: 1.97x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 617 ms: 1.78x faster                                                  |
| mdp                        | 3.97 sec                                               | 2.35 sec: 1.69x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 650 ms: 1.66x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.14 ms: 1.42x faster                                                 |
| float                      | 123 ms                                                 | 100 ms: 1.23x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 143 ms: 1.18x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.53 sec: 1.17x faster                                                |
| deepcopy                   | 468 us                                                 | 405 us: 1.16x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 45.8 us: 1.14x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 216 ms: 1.12x faster                                                  |
| pidigits                   | 250 ms                                                 | 231 ms: 1.08x faster                                                  |
| pylint                     | 465 ms                                                 | 433 ms: 1.07x faster                                                  |
| comprehensions             | 27.1 us                                                | 25.3 us: 1.07x faster                                                 |
| spectral_norm              | 156 ms                                                 | 147 ms: 1.06x faster                                                  |
| async_generators           | 589 ms                                                 | 559 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.86 us: 1.05x faster                                                 |
| regex_dna                  | 278 ms                                                 | 289 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 312 us: 1.04x slower                                                  |
| richards_super             | 72.8 ms                                                | 76.1 ms: 1.05x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 6.90 sec: 1.05x slower                                                |
| json                       | 6.85 ms                                                | 7.18 ms: 1.05x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 113 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.03 sec: 1.06x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.27 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.15 sec: 1.09x slower                                                |
| xml_etree_process          | 83.7 ms                                                | 91.5 ms: 1.09x slower                                                 |
| json_loads                 | 37.9 us                                                | 41.7 us: 1.10x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 106 ms: 1.10x slower                                                  |
| sympy_str                  | 385 ms                                                 | 426 ms: 1.11x slower                                                  |
| logging_format             | 9.59 us                                                | 10.7 us: 1.12x slower                                                 |
| html5lib                   | 88.9 ms                                                | 99.3 ms: 1.12x slower                                                 |
| fannkuch                   | 540 ms                                                 | 604 ms: 1.12x slower                                                  |
| 2to3                       | 456 ms                                                 | 511 ms: 1.12x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 249 ms: 1.12x slower                                                  |
| generators                 | 41.1 ms                                                | 46.6 ms: 1.13x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 497 us: 1.14x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.91 ms: 1.15x slower                                                 |
| richards                   | 60.3 ms                                                | 70.2 ms: 1.16x slower                                                 |
| sympy_expand               | 582 ms                                                 | 680 ms: 1.17x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 262 us: 1.17x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 79.3 ms: 1.17x slower                                                 |
| django_template            | 44.9 ms                                                | 53.0 ms: 1.18x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 29.3 ms: 1.18x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 183 ms: 1.20x slower                                                  |
| genshi_text                | 30.2 ms                                                | 37.0 ms: 1.23x slower                                                 |
| meteor_contest             | 146 ms                                                 | 181 ms: 1.24x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.8 ms: 1.24x slower                                                 |
| coroutines                 | 29.5 ms                                                | 36.6 ms: 1.24x slower                                                 |
| python_startup             | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                 |
| telco                      | 9.59 ms                                                | 12.1 ms: 1.26x slower                                                 |
| nbody                      | 119 ms                                                 | 150 ms: 1.26x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.6 ms: 1.28x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.50 ms: 1.29x slower                                                 |
| mako                       | 15.7 ms                                                | 21.4 ms: 1.36x slower                                                 |
| coverage                   | 95.4 ms                                                | 158 ms: 1.65x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 88.4 ms: 4.27x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (21): dulwich_log, sqlalchemy_declarative, raytrace, scimark_fft, nqueens, pyflate, regex_v8, sqlite_synth, logging_simple, pathlib, logging_silent, tomli_loads, scimark_sor, asyncio_websockets, bench_thread_pool, xml_etree_generate, docutils, chaos, regex_compile, sympy_integrate, go
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 76.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x