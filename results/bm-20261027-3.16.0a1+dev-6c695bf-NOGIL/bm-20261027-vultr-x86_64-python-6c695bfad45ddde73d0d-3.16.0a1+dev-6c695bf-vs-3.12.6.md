# Results vs. 3.12.6

- fork: python
- ref: 6c695bfad45ddde73d0d
- machine: linux-x86_64
- commit hash: 6c695bf
- commit date: 2026-10-27
- overall geometric mean: 1.033x slower
- HPT reliability: 78.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 291 ms: 1.11x slower                                                      |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                    |
| html5lib       | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                      |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 335 ms: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 292 ms: 1.32x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 425 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 634 ms: 1.13x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                      |
| coroutines                 | 23.9 ms                                                | 25.8 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 84.7 ms: 1.05x slower                                                     |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                      |
| nbody          | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                     |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                      |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                    |
| json_dumps           | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 97.4 ms: 1.01x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                      |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 76.1 ms: 1.29x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.07 ms: 1.27x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.8 ms: 1.39x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.33x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                     |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 127 ms: 2.50x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.80 ms: 1.92x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.53 ms: 1.65x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                      |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 335 ms: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 292 ms: 1.32x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 425 ms: 1.31x faster                                                      |
| deepcopy                   | 352 us                                                 | 272 us: 1.29x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 32.3 us: 1.25x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 136 us: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                     |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 634 ms: 1.13x faster                                                      |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                     |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                    |
| chaos                      | 62.8 ms                                                | 59.8 ms: 1.05x faster                                                     |
| scimark_fft                | 342 ms                                                 | 326 ms: 1.05x faster                                                      |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                     |
| raytrace                   | 299 ms                                                 | 291 ms: 1.03x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                    |
| pyflate                    | 448 ms                                                 | 451 ms: 1.01x slower                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 97.4 ms: 1.01x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| html5lib                   | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                     |
| float                      | 80.8 ms                                                | 84.7 ms: 1.05x slower                                                     |
| logging_simple             | 6.63 us                                                | 6.97 us: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                      |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                     |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 799 ms: 1.08x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.71 ms: 1.08x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.8 ms: 1.08x slower                                                     |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                                     |
| generators                 | 32.2 ms                                                | 34.8 ms: 1.08x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.3 ms: 1.08x slower                                                     |
| logging_format             | 7.35 us                                                | 7.97 us: 1.09x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.78 ms: 1.09x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.10x slower                                                    |
| 2to3                       | 264 ms                                                 | 291 ms: 1.11x slower                                                      |
| nqueens                    | 80.1 ms                                                | 88.7 ms: 1.11x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                      |
| sympy_str                  | 292 ms                                                 | 324 ms: 1.11x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 76.5 ms: 1.12x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                      |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                      |
| richards_super             | 51.9 ms                                                | 59.4 ms: 1.14x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.14x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| sympy_expand               | 468 ms                                                 | 543 ms: 1.16x slower                                                      |
| thrift                     | 791 us                                                 | 926 us: 1.17x slower                                                      |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                      |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.20x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                     |
| django_template            | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                     |
| fannkuch                   | 372 ms                                                 | 471 ms: 1.27x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.07 ms: 1.27x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 76.1 ms: 1.29x slower                                                     |
| nbody                      | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.8 ms: 1.39x slower                                                     |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.41 ms: 1.50x slower                                                     |
| coverage                   | 71.4 ms                                                | 118 ms: 1.65x slower                                                      |
| telco                      | 6.53 ms                                                | 176 ms: 27.00x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261027-3.16.0a1+dev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 78.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x