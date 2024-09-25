# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.04x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 422 ms: 1.08x faster                                  |
| html5lib       | 88.9 ms                                                | 93.8 ms: 1.05x slower                                 |
| tornado_http   | 266 ms                                                 | 241 ms: 1.10x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.27 sec: 1.52x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 466 ms: 1.51x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 670 ms: 1.46x faster                                  |
| async_tree_none            | 741 ms                                                 | 508 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.44x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 650 ms: 1.43x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 847 ms: 1.30x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 857 ms: 1.26x faster                                  |
| async_generators           | 589 ms                                                 | 574 ms: 1.03x faster                                  |
| coroutines                 | 29.5 ms                                                | 31.3 ms: 1.06x slower                                 |
| Geometric mean             | (ref)                                                  | 1.23x faster                                          |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 175 ms: 1.06x faster                                  |
| regex_dna      | 278 ms                                                 | 292 ms: 1.05x slower                                  |
| regex_v8       | 32.5 ms                                                | 35.4 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 47.7 us: 1.11x faster                                 |
| unpickle_pure_python | 300 us                                                 | 275 us: 1.09x faster                                  |
| xml_etree_parse      | 241 ms                                                 | 227 ms: 1.06x faster                                  |
| tomli_loads          | 2.88 sec                                               | 2.73 sec: 1.06x faster                                |
| xml_etree_generate   | 127 ms                                                 | 121 ms: 1.05x faster                                  |
| json_dumps           | 14.3 ms                                                | 15.7 ms: 1.10x slower                                 |
| unpickle_list        | 6.83 us                                                | 7.68 us: 1.12x slower                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (7): pickle, unpickle, pickle_list, xml_etree_iterparse, json_loads, pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.4 ms: 1.14x faster                                 |
| python_startup         | 23.7 ms                                                | 22.6 ms: 1.05x faster                                 |
| Geometric mean         | (ref)                                                  | 1.10x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 44.9 ms                                                | 47.1 ms: 1.05x slower                                 |
| genshi_xml      | 67.6 ms                                                | 71.8 ms: 1.06x slower                                 |
| genshi_text     | 30.2 ms                                                | 32.4 ms: 1.07x slower                                 |
| mako            | 15.7 ms                                                | 17.0 ms: 1.08x slower                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.27 sec: 1.52x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 466 ms: 1.51x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 670 ms: 1.46x faster                                  |
| async_tree_none            | 741 ms                                                 | 508 ms: 1.46x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.44x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 650 ms: 1.43x faster                                  |
| deepcopy_memo              | 52.4 us                                                | 39.8 us: 1.32x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 847 ms: 1.30x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 857 ms: 1.26x faster                                  |
| raytrace                   | 408 ms                                                 | 328 ms: 1.24x faster                                  |
| deepcopy                   | 468 us                                                 | 383 us: 1.22x faster                                  |
| comprehensions             | 27.1 us                                                | 22.4 us: 1.21x faster                                 |
| python_startup_no_site     | 17.6 ms                                                | 15.4 ms: 1.14x faster                                 |
| logging_simple             | 9.45 us                                                | 8.33 us: 1.13x faster                                 |
| pathlib                    | 31.6 ms                                                | 28.0 ms: 1.13x faster                                 |
| pickle_dict                | 52.7 us                                                | 47.7 us: 1.11x faster                                 |
| tornado_http               | 266 ms                                                 | 241 ms: 1.10x faster                                  |
| unpickle_pure_python       | 300 us                                                 | 275 us: 1.09x faster                                  |
| sympy_integrate            | 29.8 ms                                                | 27.3 ms: 1.09x faster                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 88.7 ms: 1.09x faster                                 |
| 2to3                       | 456 ms                                                 | 422 ms: 1.08x faster                                  |
| pyflate                    | 727 ms                                                 | 674 ms: 1.08x faster                                  |
| pycparser                  | 1.79 sec                                               | 1.67 sec: 1.07x faster                                |
| mdp                        | 3.97 sec                                               | 3.71 sec: 1.07x faster                                |
| sqlglot_normalize          | 157 ms                                                 | 147 ms: 1.07x faster                                  |
| regex_compile              | 187 ms                                                 | 175 ms: 1.06x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 227 ms: 1.06x faster                                  |
| sqlglot_optimize           | 76.0 ms                                                | 71.7 ms: 1.06x faster                                 |
| tomli_loads                | 2.88 sec                                               | 2.73 sec: 1.06x faster                                |
| deepcopy_reduce            | 4.04 us                                                | 3.83 us: 1.05x faster                                 |
| xml_etree_generate         | 127 ms                                                 | 121 ms: 1.05x faster                                  |
| python_startup             | 23.7 ms                                                | 22.6 ms: 1.05x faster                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.24 ms: 1.04x faster                                 |
| bpe_tokeniser              | 6.59 sec                                               | 6.31 sec: 1.04x faster                                |
| sympy_str                  | 385 ms                                                 | 370 ms: 1.04x faster                                  |
| async_generators           | 589 ms                                                 | 574 ms: 1.03x faster                                  |
| django_template            | 44.9 ms                                                | 47.1 ms: 1.05x slower                                 |
| regex_dna                  | 278 ms                                                 | 292 ms: 1.05x slower                                  |
| richards                   | 60.3 ms                                                | 63.5 ms: 1.05x slower                                 |
| html5lib                   | 88.9 ms                                                | 93.8 ms: 1.05x slower                                 |
| coroutines                 | 29.5 ms                                                | 31.3 ms: 1.06x slower                                 |
| genshi_xml                 | 67.6 ms                                                | 71.8 ms: 1.06x slower                                 |
| sympy_expand               | 582 ms                                                 | 622 ms: 1.07x slower                                  |
| genshi_text                | 30.2 ms                                                | 32.4 ms: 1.07x slower                                 |
| mako                       | 15.7 ms                                                | 17.0 ms: 1.08x slower                                 |
| regex_v8                   | 32.5 ms                                                | 35.4 ms: 1.09x slower                                 |
| json_dumps                 | 14.3 ms                                                | 15.7 ms: 1.10x slower                                 |
| json                       | 6.85 ms                                                | 7.54 ms: 1.10x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 66.6 ns: 1.11x slower                                 |
| thrift                     | 1.06 ms                                                | 1.19 ms: 1.12x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.68 us: 1.12x slower                                 |
| go                         | 172 ms                                                 | 196 ms: 1.14x slower                                  |
| telco                      | 9.59 ms                                                | 11.2 ms: 1.17x slower                                 |
| coverage                   | 95.4 ms                                                | 117 ms: 1.22x slower                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.51 ms: 1.29x slower                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                          |

Benchmark hidden because not significant (41): bench_mp_pool, pickle, unpickle, chaos, logging_silent, pickle_list, gc_traversal, nbody, xml_etree_iterparse, richards_super, sqlite_synth, asyncio_websockets, fannkuch, float, crypto_pyaes, scimark_sparse_mat_mult, pprint_safe_repr, pprint_pformat, logging_format, json_loads, nqueens, pickle_pure_python, generators, spectral_norm, scimark_lu, asyncio_tcp_ssl, docutils, sqlglot_parse, scimark_sor, pidigits, scimark_fft, meteor_contest, bench_thread_pool, hexiom, xml_etree_process, regex_effbot, deltablue, sympy_sum, pylint, typing_runtime_protocols, asyncio_tcp
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.83% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x