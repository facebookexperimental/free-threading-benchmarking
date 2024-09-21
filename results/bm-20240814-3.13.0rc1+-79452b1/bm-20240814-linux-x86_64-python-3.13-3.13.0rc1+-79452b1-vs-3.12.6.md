# Results vs. 3.12.6

- fork: python
- ref: 3.13
- machine: linux-x86_64
- commit hash: 79452b1
- commit date: 2024-08-14
- overall geometric mean: 1.02x faster
- HPT reliability: 99.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| chameleon      | 9.31 ms                                                | 9.84 ms: 1.06x slower                                   |
| html5lib       | 88.9 ms                                                | 98.1 ms: 1.10x slower                                   |
| tornado_http   | 266 ms                                                 | 248 ms: 1.07x faster                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                            |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 672 ms: 1.38x faster                                    |
| async_tree_none_tg         | 704 ms                                                 | 521 ms: 1.35x faster                                    |
| async_tree_io              | 1.85 sec                                               | 1.38 sec: 1.34x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.46 sec: 1.33x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 745 ms: 1.31x faster                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 849 ms: 1.30x faster                                    |
| async_tree_none            | 741 ms                                                 | 576 ms: 1.29x faster                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 899 ms: 1.20x faster                                    |
| asyncio_websockets         | 748 ms                                                 | 772 ms: 1.03x slower                                    |
| asyncio_tcp                | 923 ms                                                 | 985 ms: 1.07x slower                                    |
| Geometric mean             | (ref)                                                  | 1.17x faster                                            |

Benchmark hidden because not significant (3): coroutines, asyncio_tcp_ssl, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.84 ms: 1.06x faster                                   |
| regex_compile  | 187 ms                                                 | 177 ms: 1.05x faster                                    |
| regex_dna      | 278 ms                                                 | 288 ms: 1.04x slower                                    |
| Geometric mean | (ref)                                                  | 1.02x faster                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| pickle_dict    | 52.7 us                                                | 46.5 us: 1.13x faster                                   |
| pickle         | 16.4 us                                                | 15.4 us: 1.07x faster                                   |
| json_loads     | 37.9 us                                                | 36.1 us: 1.05x faster                                   |
| tomli_loads    | 2.88 sec                                               | 2.80 sec: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                            |

Benchmark hidden because not significant (10): pickle_pure_python, unpickle_list, pickle_list, xml_etree_parse, unpickle_pure_python, unpickle, xml_etree_generate, xml_etree_process, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.6 ms: 1.20x faster                                   |
| python_startup         | 23.7 ms                                                | 22.0 ms: 1.08x faster                                   |
| Geometric mean         | (ref)                                                  | 1.14x faster                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| django_template | 44.9 ms                                                | 46.9 ms: 1.04x slower                                   |
| Geometric mean  | (ref)                                                  | 1.03x slower                                            |

Benchmark hidden because not significant (3): genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 672 ms: 1.38x faster                                    |
| async_tree_none_tg         | 704 ms                                                 | 521 ms: 1.35x faster                                    |
| async_tree_io              | 1.85 sec                                               | 1.38 sec: 1.34x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.46 sec: 1.33x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 745 ms: 1.31x faster                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 849 ms: 1.30x faster                                    |
| comprehensions             | 27.1 us                                                | 20.9 us: 1.30x faster                                   |
| async_tree_none            | 741 ms                                                 | 576 ms: 1.29x faster                                    |
| python_startup_no_site     | 17.6 ms                                                | 14.6 ms: 1.20x faster                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 899 ms: 1.20x faster                                    |
| raytrace                   | 408 ms                                                 | 350 ms: 1.17x faster                                    |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.06 ms: 1.14x faster                                   |
| pickle_dict                | 52.7 us                                                | 46.5 us: 1.13x faster                                   |
| pyflate                    | 727 ms                                                 | 661 ms: 1.10x faster                                    |
| nqueens                    | 117 ms                                                 | 108 ms: 1.08x faster                                    |
| pathlib                    | 31.6 ms                                                | 29.3 ms: 1.08x faster                                   |
| sqlglot_normalize          | 157 ms                                                 | 146 ms: 1.08x faster                                    |
| python_startup             | 23.7 ms                                                | 22.0 ms: 1.08x faster                                   |
| crypto_pyaes               | 107 ms                                                 | 99.8 ms: 1.08x faster                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 89.9 ms: 1.07x faster                                   |
| tornado_http               | 266 ms                                                 | 248 ms: 1.07x faster                                    |
| logging_silent             | 139 ns                                                 | 130 ns: 1.07x faster                                    |
| float                      | 123 ms                                                 | 115 ms: 1.07x faster                                    |
| bench_mp_pool              | 20.7 ms                                                | 19.4 ms: 1.07x faster                                   |
| pickle                     | 16.4 us                                                | 15.4 us: 1.07x faster                                   |
| regex_effbot               | 5.13 ms                                                | 4.84 ms: 1.06x faster                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.25 sec: 1.05x faster                                  |
| regex_compile              | 187 ms                                                 | 177 ms: 1.05x faster                                    |
| generators                 | 41.1 ms                                                | 39.2 ms: 1.05x faster                                   |
| scimark_fft                | 500 ms                                                 | 477 ms: 1.05x faster                                    |
| sympy_str                  | 385 ms                                                 | 367 ms: 1.05x faster                                    |
| json_loads                 | 37.9 us                                                | 36.1 us: 1.05x faster                                   |
| mdp                        | 3.97 sec                                               | 3.80 sec: 1.05x faster                                  |
| json                       | 6.85 ms                                                | 6.55 ms: 1.05x faster                                   |
| tomli_loads                | 2.88 sec                                               | 2.80 sec: 1.03x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 772 ms: 1.03x slower                                    |
| regex_dna                  | 278 ms                                                 | 288 ms: 1.04x slower                                    |
| django_template            | 44.9 ms                                                | 46.9 ms: 1.04x slower                                   |
| sqlite_synth               | 3.87 us                                                | 4.07 us: 1.05x slower                                   |
| chameleon                  | 9.31 ms                                                | 9.84 ms: 1.06x slower                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.27 us: 1.06x slower                                   |
| asyncio_tcp                | 923 ms                                                 | 985 ms: 1.07x slower                                    |
| deltablue                  | 4.27 ms                                                | 4.56 ms: 1.07x slower                                   |
| meteor_contest             | 146 ms                                                 | 157 ms: 1.07x slower                                    |
| sympy_expand               | 582 ms                                                 | 631 ms: 1.08x slower                                    |
| richards                   | 60.3 ms                                                | 65.8 ms: 1.09x slower                                   |
| html5lib                   | 88.9 ms                                                | 98.1 ms: 1.10x slower                                   |
| aiohttp                    | 1.99 ms                                                | 2.23 ms: 1.12x slower                                   |
| go                         | 172 ms                                                 | 195 ms: 1.14x slower                                    |
| coverage                   | 95.4 ms                                                | 110 ms: 1.15x slower                                    |
| flaskblogging              | 7.48 ms                                                | 8.78 ms: 1.17x slower                                   |
| telco                      | 9.59 ms                                                | 11.4 ms: 1.19x slower                                   |
| unpack_sequence            | 60.2 ns                                                | 73.9 ns: 1.23x slower                                   |
| gunicorn                   | 1.81 ms                                                | 2.25 ms: 1.24x slower                                   |
| create_gc_cycles           | 1.94 ms                                                | 2.46 ms: 1.27x slower                                   |
| Geometric mean             | (ref)                                                  | 1.02x faster                                            |

Benchmark hidden because not significant (46): logging_simple, pickle_pure_python, sympy_sum, typing_runtime_protocols, 2to3, unpickle_list, pickle_list, xml_etree_parse, sqlglot_transpile, deepcopy_memo, unpickle_pure_python, logging_format, coroutines, pidigits, pprint_safe_repr, asyncio_tcp_ssl, dulwich_log, sympy_integrate, chaos, regex_v8, dask, docutils, sqlglot_optimize, async_generators, fannkuch, unpickle, sqlglot_parse, gc_traversal, pprint_pformat, hexiom, genshi_xml, scimark_lu, pylint, xml_etree_generate, mako, spectral_norm, xml_etree_process, scimark_sor, deepcopy, nbody, json_dumps, xml_etree_iterparse, scimark_sparse_mat_mult, richards_super, genshi_text, thrift
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.63% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x