# Results vs. 3.12.6

- fork: nascheme
- ref: gh_132380_tp_getattr
- machine: linux-x86_64
- commit hash: 04ccde3
- commit date: 2025-06-05
- overall geometric mean: 1.015x faster
- HPT reliability: 89.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                    |
| html5lib       | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                    |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                    |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                   |
| pidigits       | 184 ms                                                 | 189 ms: 1.02x slower                                                    |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.21x faster                                                   |
| regex_dna      | 168 ms                                                 | 170 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.5 ms: 1.10x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.1 ms: 1.16x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                   |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 58.4 ms: 1.16x slower                                                   |
| django_template | 34.7 ms                                                | 40.6 ms: 1.17x slower                                                   |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                                   |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                    |
| deepcopy                   | 352 us                                                 | 291 us: 1.21x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.21x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                   |
| float                      | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                   |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.4 us: 1.14x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 70.9 ms: 1.11x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.5 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                    |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                    |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                                   |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                   |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                    |
| regex_dna                  | 168 ms                                                 | 170 ms: 1.01x slower                                                    |
| pidigits                   | 184 ms                                                 | 189 ms: 1.02x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.35 ms: 1.03x slower                                                   |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                    |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                                   |
| html5lib                   | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                    |
| json                       | 5.02 ms                                                | 5.29 ms: 1.05x slower                                                   |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                    |
| nqueens                    | 80.1 ms                                                | 85.4 ms: 1.07x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                    |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                    |
| scimark_fft                | 342 ms                                                 | 370 ms: 1.08x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                    |
| thrift                     | 791 us                                                 | 868 us: 1.10x slower                                                    |
| richards                   | 45.9 ms                                                | 51.0 ms: 1.11x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 76.9 ms: 1.12x slower                                                   |
| richards_super             | 51.9 ms                                                | 58.7 ms: 1.13x slower                                                   |
| sympy_expand               | 468 ms                                                 | 531 ms: 1.14x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 187 us: 1.15x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.63 us: 1.15x slower                                                   |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                    |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 58.4 ms: 1.16x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.1 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 866 ms: 1.17x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                   |
| django_template            | 34.7 ms                                                | 40.6 ms: 1.17x slower                                                   |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.79 sec: 1.18x slower                                                  |
| logging_format             | 7.35 us                                                | 8.69 us: 1.18x slower                                                   |
| fannkuch                   | 372 ms                                                 | 457 ms: 1.23x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.56 ms: 1.26x slower                                                   |
| telco                      | 6.53 ms                                                | 8.56 ms: 1.31x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.46 ms: 1.33x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                                    |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                   |
| coverage                   | 71.4 ms                                                | 112 ms: 1.56x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.10 ms: 3.30x slower                                                   |
| logging_silent             | 109 ns                                                 | 528 ns: 4.84x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 102 ms: 9.44x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (5): chaos, regex_compile, coroutines, docutils, regex_v8
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 89.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x