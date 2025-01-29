# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_128563_revert
- machine: linux-x86_64
- commit hash: 8014514
- commit date: 2025-01-29
- overall geometric mean: 1.073x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                                |
| html5lib       | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 573 ms: 1.59x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 507 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                  |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| float          | 77.5 ms                                                      | 76.6 ms: 1.01x faster                                                 |
| nbody          | 85.1 ms                                                      | 133 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                 |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 95.9 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.3 ms: 1.15x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                |
| unpickle_pure_python | 210 us                                                       | 247 us: 1.17x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 365 us: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                                 |
| django_template | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.75 ms: 1.79x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 573 ms: 1.59x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 507 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                  |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                  |
| deepcopy                   | 355 us                                                       | 307 us: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 37.5 us: 1.04x faster                                                 |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                 |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| float                      | 77.5 ms                                                      | 76.6 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.16 us: 1.02x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.39 ms: 1.04x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.62 sec: 1.04x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.04x slower                                                |
| html5lib                   | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                                |
| logging_silent             | 103 ns                                                       | 111 ns: 1.08x slower                                                  |
| pyflate                    | 449 ms                                                       | 485 ms: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 81.7 ms: 1.09x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.5 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 807 ms: 1.09x slower                                                  |
| scimark_fft                | 349 ms                                                       | 386 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.11x slower                                                |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 95.9 ms: 1.12x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.65 sec: 1.13x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.94 ms: 1.14x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.3 ms: 1.15x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 60.8 ms: 1.15x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                |
| thrift                     | 778 us                                                       | 904 us: 1.16x slower                                                  |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                                  |
| coverage                   | 83.0 ms                                                      | 97.3 ms: 1.17x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 247 us: 1.17x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.26 us: 1.18x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 184 ms: 1.18x slower                                                  |
| sympy_expand               | 457 ms                                                       | 544 ms: 1.19x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.17 us: 1.19x slower                                                 |
| comprehensions             | 16.5 us                                                      | 19.7 us: 1.20x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 23.8 ms: 1.20x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                                  |
| sympy_str                  | 275 ms                                                       | 331 ms: 1.21x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.88 ms: 1.21x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.27 ms: 1.21x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 95.3 ms: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.72 ms: 1.21x slower                                                 |
| chaos                      | 57.3 ms                                                      | 69.8 ms: 1.22x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                                 |
| richards                   | 45.2 ms                                                      | 55.9 ms: 1.24x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 365 us: 1.24x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.1 ms: 1.24x slower                                                 |
| django_template            | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.56 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 195 us: 1.26x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| richards_super             | 51.6 ms                                                      | 65.5 ms: 1.27x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 27.4 ms: 1.27x slower                                                 |
| raytrace                   | 253 ms                                                       | 328 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 88.4 ms: 1.30x slower                                                 |
| fannkuch                   | 370 ms                                                       | 483 ms: 1.31x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.59 ms: 1.47x slower                                                 |
| nbody                      | 85.1 ms                                                      | 133 ms: 1.56x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 94.4 ms: 8.59x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                          |

Benchmark hidden because not significant (2): pylint, async_generators
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250129-3.14.0a4+-8014514-NOGIL/bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x