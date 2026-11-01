# Results vs. 3.12.6

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: linux-x86_64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.032x slower
- HPT reliability: 70.38%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 291 ms: 1.10x slower                                                      |
| docutils       | 2.64 sec                                               | 2.89 sec: 1.10x slower                                                    |
| html5lib       | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 697 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 712 ms: 1.52x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                      |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 417 ms: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 292 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 589 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                      |
| float          | 80.8 ms                                                | 84.7 ms: 1.05x slower                                                     |
| nbody          | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| Geometric mean | (ref)                                                  | 1.12x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 180 ms: 1.08x slower                                                      |
| regex_compile  | 142 ms                                                 | 169 ms: 1.18x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.09x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                      |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 75.8 ms: 1.29x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.09 ms: 1.27x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.8 ms: 1.39x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.33x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                     |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 127 ms: 2.51x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.80 ms: 1.92x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.55 ms: 1.65x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 697 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 712 ms: 1.52x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                      |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 417 ms: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 292 ms: 1.32x faster                                                      |
| deepcopy                   | 352 us                                                 | 270 us: 1.30x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 589 ms: 1.23x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 33.3 us: 1.21x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 142 us: 1.15x faster                                                      |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                      |
| comprehensions             | 19.8 us                                                | 17.7 us: 1.12x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.0 ms: 1.11x faster                                                     |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                    |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.06x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                     |
| scimark_fft                | 342 ms                                                 | 328 ms: 1.04x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                    |
| chaos                      | 62.8 ms                                                | 60.6 ms: 1.04x faster                                                     |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| pyflate                    | 448 ms                                                 | 445 ms: 1.01x faster                                                      |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                      |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                      |
| html5lib                   | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                                     |
| logging_simple             | 6.63 us                                                | 6.93 us: 1.05x slower                                                     |
| float                      | 80.8 ms                                                | 84.7 ms: 1.05x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.49 ms: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.08x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                     |
| logging_format             | 7.35 us                                                | 7.93 us: 1.08x slower                                                     |
| json                       | 5.02 ms                                                | 5.44 ms: 1.08x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.09x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.74 ms: 1.09x slower                                                     |
| nqueens                    | 80.1 ms                                                | 87.1 ms: 1.09x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 812 ms: 1.09x slower                                                      |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.89 sec: 1.10x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 183 ms: 1.10x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.85 ms: 1.10x slower                                                     |
| 2to3                       | 264 ms                                                 | 291 ms: 1.10x slower                                                      |
| sympy_str                  | 292 ms                                                 | 323 ms: 1.11x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 77.5 ms: 1.13x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.14x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 53.2 ms: 1.16x slower                                                     |
| sympy_expand               | 468 ms                                                 | 542 ms: 1.16x slower                                                      |
| thrift                     | 791 us                                                 | 918 us: 1.16x slower                                                      |
| richards_super             | 51.9 ms                                                | 60.9 ms: 1.17x slower                                                     |
| regex_compile              | 142 ms                                                 | 169 ms: 1.18x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| django_template            | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                     |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.32 ms: 1.21x slower                                                     |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.09 ms: 1.27x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 75.8 ms: 1.29x slower                                                     |
| nbody                      | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.8 ms: 1.39x slower                                                     |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.41 ms: 1.50x slower                                                     |
| coverage                   | 71.4 ms                                                | 117 ms: 1.64x slower                                                      |
| telco                      | 6.53 ms                                                | 175 ms: 26.85x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_iterparse
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261031-3.16.0a1+dev-410fdda-NOGIL/bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x slower

# HPT report

- Reliability score: 70.38% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x