# Results vs. 3.13.0rc2

- fork: python
- ref: 3945eaf2fcd9cbc3f306
- machine: linux-x86_64
- commit hash: 3945eaf
- commit date: 2026-11-03
- overall geometric mean: 1.067x slower
- HPT reliability: 91.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 291 ms: 1.12x slower                                                      |
| docutils       | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                    |
| html5lib       | 67.0 ms                                                      | 65.1 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                        | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 705 ms: 1.30x faster                                                      |
| async_generators           | 377 ms                                                       | 295 ms: 1.28x faster                                                      |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 574 ms: 1.16x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 571 ms: 1.12x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                      |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 502 ms: 1.04x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.10x faster                                                              |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                      |
| float          | 77.5 ms                                                      | 84.0 ms: 1.08x slower                                                     |
| nbody          | 85.1 ms                                                      | 117 ms: 1.37x slower                                                      |
| Geometric mean | (ref)                                                        | 1.09x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                     |
| regex_effbot   | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                     |
| regex_compile  | 132 ms                                                       | 171 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 10.1 ms: 1.05x faster                                                     |
| tomli_loads          | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.2 ms: 1.01x slower                                                     |
| xml_etree_parse      | 136 ms                                                       | 145 ms: 1.07x slower                                                      |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 240 us: 1.14x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 352 us: 1.20x slower                                                      |
| xml_etree_process    | 59.3 ms                                                      | 75.7 ms: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 8.93 ms: 1.21x slower                                                     |
| python_startup         | 11.0 ms                                                      | 13.4 ms: 1.22x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.22x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                                     |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 128 ms: 2.47x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.82x faster                                                    |
| gc_traversal               | 3.14 ms                                                      | 1.82 ms: 1.73x faster                                                     |
| bench_mp_pool              | 11.0 ms                                                      | 6.65 ms: 1.65x faster                                                     |
| deepcopy                   | 355 us                                                       | 274 us: 1.30x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 705 ms: 1.30x faster                                                      |
| async_generators           | 377 ms                                                       | 295 ms: 1.28x faster                                                      |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                      |
| deepcopy_memo              | 39.1 us                                                      | 33.3 us: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 574 ms: 1.16x faster                                                      |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                      |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 571 ms: 1.12x faster                                                      |
| typing_runtime_protocols   | 155 us                                                       | 139 us: 1.11x faster                                                      |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                      |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.06x faster                                                     |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 10.1 ms: 1.05x faster                                                     |
| scimark_fft                | 349 ms                                                       | 334 ms: 1.05x faster                                                      |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 502 ms: 1.04x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 3.00 us: 1.04x faster                                                     |
| dulwich_log                | 74.8 ms                                                      | 72.5 ms: 1.03x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                     |
| html5lib                   | 67.0 ms                                                      | 65.1 ms: 1.03x faster                                                     |
| tomli_loads                | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.36 sec: 1.02x faster                                                    |
| pyflate                    | 449 ms                                                       | 441 ms: 1.02x faster                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.35 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 96.2 ms: 1.01x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                    |
| logging_silent             | 103 ns                                                       | 109 ns: 1.06x slower                                                      |
| xml_etree_parse            | 136 ms                                                       | 145 ms: 1.07x slower                                                      |
| chaos                      | 57.3 ms                                                      | 61.2 ms: 1.07x slower                                                     |
| docutils                   | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                    |
| float                      | 77.5 ms                                                      | 84.0 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.16 ms: 1.10x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 809 ms: 1.10x slower                                                      |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.10x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 6.65 ms: 1.11x slower                                                     |
| json                       | 4.93 ms                                                      | 5.48 ms: 1.11x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.12x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 88.0 ms: 1.12x slower                                                     |
| 2to3                       | 260 ms                                                       | 291 ms: 1.12x slower                                                      |
| sympy_integrate            | 19.8 ms                                                      | 22.2 ms: 1.12x slower                                                     |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 240 us: 1.14x slower                                                      |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.14x slower                                                      |
| logging_simple             | 6.16 us                                                      | 7.10 us: 1.15x slower                                                     |
| richards                   | 45.2 ms                                                      | 52.9 ms: 1.17x slower                                                     |
| raytrace                   | 253 ms                                                       | 296 ms: 1.17x slower                                                      |
| logging_format             | 6.84 us                                                      | 8.03 us: 1.17x slower                                                     |
| richards_super             | 51.6 ms                                                      | 60.7 ms: 1.18x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.1 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                      |
| sympy_expand               | 457 ms                                                       | 541 ms: 1.18x slower                                                      |
| sympy_str                  | 275 ms                                                       | 325 ms: 1.18x slower                                                      |
| generators                 | 28.8 ms                                                      | 34.1 ms: 1.18x slower                                                     |
| thrift                     | 778 us                                                       | 927 us: 1.19x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.19x slower                                                      |
| pickle_pure_python         | 294 us                                                       | 352 us: 1.20x slower                                                      |
| django_template            | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 8.93 ms: 1.21x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.80 ms: 1.22x slower                                                     |
| python_startup             | 11.0 ms                                                      | 13.4 ms: 1.22x slower                                                     |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                      |
| fannkuch                   | 370 ms                                                       | 468 ms: 1.27x slower                                                      |
| xml_etree_process          | 59.3 ms                                                      | 75.7 ms: 1.27x slower                                                     |
| regex_compile              | 132 ms                                                       | 171 ms: 1.29x slower                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 88.5 ms: 1.30x slower                                                     |
| nbody                      | 85.1 ms                                                      | 117 ms: 1.37x slower                                                      |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                     |
| coverage                   | 83.0 ms                                                      | 119 ms: 1.44x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.40 ms: 1.53x slower                                                     |
| telco                      | 7.82 ms                                                      | 176 ms: 22.45x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                              |

Benchmark hidden because not significant (2): async_tree_none_tg, regex_dna
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261103-3.16.0a1+dev-3945eaf-NOGIL/bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x slower

# HPT report

- Reliability score: 91.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x