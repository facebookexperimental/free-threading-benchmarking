# Results vs. 3.13.0rc2

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: linux-x86_64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.049x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                      |
| docutils       | 2.62 sec                                                     | 2.33 sec: 1.12x faster                                                    |
| html5lib       | 67.0 ms                                                      | 57.6 ms: 1.16x faster                                                     |
| Geometric mean | (ref)                                                        | 1.10x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 377 ms                                                       | 226 ms: 1.67x faster                                                      |
| async_tree_io              | 876 ms                                                       | 655 ms: 1.34x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 348 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                      |
| async_tree_none            | 354 ms                                                       | 277 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 520 ms: 1.23x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 282 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 349 ms: 1.19x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.15x faster                                                      |
| float          | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                     |
| nbody          | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                        | 1.05x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                     |
| regex_dna      | 180 ms                                                       | 179 ms: 1.00x faster                                                      |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.20 ms: 1.14x faster                                                     |
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                     |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                      |
| json_loads           | 27.0 us                                                      | 27.3 us: 1.01x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 87.2 ms: 1.02x slower                                                     |
| xml_etree_parse      | 136 ms                                                       | 141 ms: 1.04x slower                                                      |
| xml_etree_process    | 59.3 ms                                                      | 62.0 ms: 1.04x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.55 ms: 1.02x slower                                                     |
| python_startup         | 11.0 ms                                                      | 11.5 ms: 1.04x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.03x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                     |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 108 ms: 2.93x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.06x faster                                                    |
| async_generators           | 377 ms                                                       | 226 ms: 1.67x faster                                                      |
| deepcopy                   | 355 us                                                       | 233 us: 1.52x faster                                                      |
| deepcopy_memo              | 39.1 us                                                      | 27.7 us: 1.41x faster                                                     |
| typing_runtime_protocols   | 155 us                                                       | 111 us: 1.40x faster                                                      |
| go                         | 141 ms                                                       | 105 ms: 1.35x faster                                                      |
| async_tree_io              | 876 ms                                                       | 655 ms: 1.34x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 348 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                      |
| async_tree_none            | 354 ms                                                       | 277 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 520 ms: 1.23x faster                                                      |
| spectral_norm              | 111 ms                                                       | 91.5 ms: 1.21x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                     |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 282 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 349 ms: 1.19x faster                                                      |
| pyflate                    | 449 ms                                                       | 385 ms: 1.16x faster                                                      |
| html5lib                   | 67.0 ms                                                      | 57.6 ms: 1.16x faster                                                     |
| pidigits                   | 217 ms                                                       | 188 ms: 1.15x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 9.20 ms: 1.14x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.33 sec: 1.12x faster                                                    |
| scimark_fft                | 349 ms                                                       | 312 ms: 1.12x faster                                                      |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                     |
| dulwich_log                | 74.8 ms                                                      | 68.0 ms: 1.10x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                     |
| float                      | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                    |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                     |
| chaos                      | 57.3 ms                                                      | 54.5 ms: 1.05x faster                                                     |
| logging_silent             | 103 ns                                                       | 97.9 ns: 1.05x faster                                                     |
| nqueens                    | 78.6 ms                                                      | 75.5 ms: 1.04x faster                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.2 ms: 1.03x faster                                                     |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 66.2 ms: 1.03x faster                                                     |
| sympy_integrate            | 19.8 ms                                                      | 19.4 ms: 1.02x faster                                                     |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                      |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 730 ms: 1.01x faster                                                      |
| richards_super             | 51.6 ms                                                      | 51.1 ms: 1.01x faster                                                     |
| richards                   | 45.2 ms                                                      | 44.8 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.67 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                    |
| coverage                   | 83.0 ms                                                      | 82.5 ms: 1.01x faster                                                     |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.00x faster                                                      |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                      |
| fannkuch                   | 370 ms                                                       | 373 ms: 1.01x slower                                                      |
| json_loads                 | 27.0 us                                                      | 27.3 us: 1.01x slower                                                     |
| logging_simple             | 6.16 us                                                      | 6.24 us: 1.01x slower                                                     |
| meteor_contest             | 102 ms                                                       | 103 ms: 1.01x slower                                                      |
| thrift                     | 778 us                                                       | 789 us: 1.01x slower                                                      |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.01x slower                                                     |
| logging_format             | 6.84 us                                                      | 6.97 us: 1.02x slower                                                     |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.55 ms: 1.02x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 87.2 ms: 1.02x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                      |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                     |
| sympy_str                  | 275 ms                                                       | 283 ms: 1.03x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                     |
| xml_etree_parse            | 136 ms                                                       | 141 ms: 1.04x slower                                                      |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 62.0 ms: 1.04x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                      |
| python_startup             | 11.0 ms                                                      | 11.5 ms: 1.04x slower                                                     |
| nbody                      | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                     |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                     |
| sympy_expand               | 457 ms                                                       | 483 ms: 1.06x slower                                                      |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                                      |
| scimark_lu                 | 113 ms                                                       | 121 ms: 1.08x slower                                                      |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 3.61 ms: 1.15x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                     |
| telco                      | 7.82 ms                                                      | 160 ms: 20.49x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                      | 233 ms: 21.18x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261031-3.16.0a1+dev-410fdda/bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x