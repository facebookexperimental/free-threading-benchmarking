# Results vs. 3.12.6

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: linux-x86_64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.044x slower
- HPT reliability: 84.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 294 ms: 1.11x slower                                                      |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                    |
| html5lib       | 63.6 ms                                                | 64.3 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 710 ms: 1.56x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 409 ms: 1.37x faster                                                      |
| async_tree_none            | 464 ms                                                 | 346 ms: 1.34x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 340 ms: 1.31x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 636 ms: 1.12x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 507 ms: 1.02x faster                                                      |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                      |
| coroutines                 | 23.9 ms                                                | 26.5 ms: 1.11x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 83.8 ms: 1.04x slower                                                     |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                      |
| nbody          | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                      |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 333 us: 1.08x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                      |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.18x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 75.7 ms: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                     |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.9 ms: 1.21x slower                                                     |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 131 ms: 2.43x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.71 ms: 1.61x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 710 ms: 1.56x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 409 ms: 1.37x faster                                                      |
| async_tree_none            | 464 ms                                                 | 346 ms: 1.34x faster                                                      |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 340 ms: 1.31x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 33.5 us: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 617 ms: 1.17x faster                                                      |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 1.95 us: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 636 ms: 1.12x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 71.4 ms: 1.10x faster                                                     |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                    |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.93 us: 1.05x faster                                                     |
| chaos                      | 62.8 ms                                                | 59.8 ms: 1.05x faster                                                     |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                     |
| scimark_fft                | 342 ms                                                 | 332 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 507 ms: 1.02x faster                                                      |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                      |
| html5lib                   | 63.6 ms                                                | 64.3 ms: 1.01x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                     |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                                      |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| float                      | 80.8 ms                                                | 83.8 ms: 1.04x slower                                                     |
| generators                 | 32.2 ms                                                | 34.2 ms: 1.06x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.61 ms: 1.07x slower                                                     |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 333 us: 1.08x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.73 ms: 1.08x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                      |
| json                       | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                     |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                                     |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                      |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.10x slower                                                      |
| logging_format             | 7.35 us                                                | 8.08 us: 1.10x slower                                                     |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                      |
| nqueens                    | 80.1 ms                                                | 88.1 ms: 1.10x slower                                                     |
| sympy_str                  | 292 ms                                                 | 322 ms: 1.11x slower                                                      |
| coroutines                 | 23.9 ms                                                | 26.5 ms: 1.11x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 825 ms: 1.11x slower                                                      |
| 2to3                       | 264 ms                                                 | 294 ms: 1.11x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 76.7 ms: 1.12x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.71 sec: 1.13x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 86.8 ms: 1.13x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.00 ms: 1.14x slower                                                     |
| sympy_expand               | 468 ms                                                 | 533 ms: 1.14x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                      |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 53.2 ms: 1.16x slower                                                     |
| thrift                     | 791 us                                                 | 920 us: 1.16x slower                                                      |
| richards_super             | 51.9 ms                                                | 61.0 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.18x slower                                                      |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                      |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| django_template            | 34.7 ms                                                | 41.9 ms: 1.21x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                     |
| fannkuch                   | 372 ms                                                 | 469 ms: 1.26x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 75.7 ms: 1.28x slower                                                     |
| nbody                      | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                     |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| coverage                   | 71.4 ms                                                | 115 ms: 1.62x slower                                                      |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.64 ms: 1.74x slower                                                     |
| telco                      | 6.53 ms                                                | 177 ms: 27.17x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_iterparse, pyflate
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261013-3.16.0a1+dev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 84.46% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x