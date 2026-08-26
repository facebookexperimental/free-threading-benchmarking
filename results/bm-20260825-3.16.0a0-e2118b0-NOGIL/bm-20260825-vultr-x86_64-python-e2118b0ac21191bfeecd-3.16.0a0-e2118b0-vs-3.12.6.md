# Results vs. 3.12.6

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: linux-x86_64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.036x slower
- HPT reliability: 81.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 694 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 704 ms: 1.54x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 418 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 584 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 597 ms: 1.20x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| async_generators           | 384 ms                                                 | 414 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 83.9 ms: 1.04x slower                                                 |
| nbody          | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| json_dumps           | 10.4 ms                                                | 10.1 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 95.3 ms: 1.01x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 333 us: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 75.6 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.87 ms: 1.38x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 130 ms: 2.44x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.97x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                |
| bench_mp_pool              | 10.8 ms                                                | 6.71 ms: 1.61x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 694 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 704 ms: 1.54x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 418 ms: 1.33x faster                                                  |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.1 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 584 ms: 1.24x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 597 ms: 1.20x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.7 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 1.95 us: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.12x faster                                                 |
| scimark_sor                | 130 ms                                                 | 118 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                  |
| chaos                      | 62.8 ms                                                | 60.5 ms: 1.04x faster                                                 |
| raytrace                   | 299 ms                                                 | 291 ms: 1.03x faster                                                  |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 10.1 ms: 1.02x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.03 us: 1.02x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 95.3 ms: 1.01x faster                                                 |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 339 ms: 1.01x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| pyflate                    | 448 ms                                                 | 454 ms: 1.01x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| float                      | 80.8 ms                                                | 83.9 ms: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.51 ms: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.67 ms: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.10 us: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                  |
| async_generators           | 384 ms                                                 | 414 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 333 us: 1.08x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 807 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.2 ms: 1.09x slower                                                 |
| sympy_str                  | 292 ms                                                 | 320 ms: 1.10x slower                                                  |
| logging_format             | 7.35 us                                                | 8.08 us: 1.10x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                |
| sympy_sum                  | 166 ms                                                 | 183 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.10x slower                                                |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                  |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 76.6 ms: 1.12x slower                                                 |
| richards                   | 45.9 ms                                                | 52.2 ms: 1.14x slower                                                 |
| sympy_expand               | 468 ms                                                 | 538 ms: 1.15x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.1 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 88.9 ms: 1.16x slower                                                 |
| thrift                     | 791 us                                                 | 928 us: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                 |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.22 ms: 1.19x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                  |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 75.6 ms: 1.28x slower                                                 |
| nbody                      | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.87 ms: 1.38x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                                 |
| coverage                   | 71.4 ms                                                | 115 ms: 1.61x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.80x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (2): pidigits, pycparser
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x slower

# HPT report

- Reliability score: 81.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x