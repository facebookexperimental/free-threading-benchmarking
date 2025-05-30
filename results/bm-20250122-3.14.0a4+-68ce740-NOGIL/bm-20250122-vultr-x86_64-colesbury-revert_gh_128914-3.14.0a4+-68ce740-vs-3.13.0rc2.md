# Results vs. 3.13.0rc2

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.086x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 305 ms: 1.17x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                |
| html5lib       | 67.0 ms                                                      | 71.2 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float          | 77.5 ms                                                      | 77.1 ms: 1.00x faster                                                 |
| nbody          | 85.1 ms                                                      | 136 ms: 1.60x slower                                                  |
| Geometric mean | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                 |
| regex_compile  | 132 ms                                                       | 152 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.8 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                 |
| json_loads           | 27.0 us                                                      | 30.8 us: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                                |
| unpickle_pure_python | 210 us                                                       | 250 us: 1.19x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.9 ms: 1.22x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.9 ms: 1.23x slower                                                 |
| django_template | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                 |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| deepcopy                   | 355 us                                                       | 314 us: 1.13x faster                                                  |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.8 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.02x faster                                                  |
| go                         | 141 ms                                                       | 138 ms: 1.02x faster                                                  |
| scimark_sor                | 134 ms                                                       | 132 ms: 1.02x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| float                      | 77.5 ms                                                      | 77.1 ms: 1.00x faster                                                 |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.00x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.36 ms: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.23 us: 1.04x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.34 ms: 1.06x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 71.2 ms: 1.06x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                |
| json                       | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.51 ms: 1.09x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.4 ms: 1.09x slower                                                 |
| logging_silent             | 103 ns                                                       | 113 ns: 1.10x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.4 ms: 1.10x slower                                                 |
| pyflate                    | 449 ms                                                       | 496 ms: 1.10x slower                                                  |
| scimark_fft                | 349 ms                                                       | 389 ms: 1.11x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 830 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.8 us: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                  |
| regex_compile              | 132 ms                                                       | 152 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.72 sec: 1.15x slower                                                |
| mdp                        | 2.36 sec                                                     | 2.70 sec: 1.15x slower                                                |
| thrift                     | 778 us                                                       | 898 us: 1.15x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.48 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| 2to3                       | 260 ms                                                       | 305 ms: 1.17x slower                                                  |
| coverage                   | 83.0 ms                                                      | 97.5 ms: 1.17x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 250 us: 1.19x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.34 us: 1.19x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                  |
| sympy_expand               | 457 ms                                                       | 549 ms: 1.20x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 136 ms: 1.21x slower                                                  |
| chaos                      | 57.3 ms                                                      | 69.3 ms: 1.21x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.29 ms: 1.22x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                 |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.37 us: 1.22x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.9 ms: 1.22x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 59.9 ms: 1.23x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 97.1 ms: 1.24x slower                                                 |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                                 |
| comprehensions             | 16.5 us                                                      | 20.6 us: 1.25x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.0 ms: 1.25x slower                                                 |
| richards_super             | 51.6 ms                                                      | 64.8 ms: 1.26x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.96 ms: 1.26x slower                                                 |
| django_template            | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.26x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                  |
| fannkuch                   | 370 ms                                                       | 481 ms: 1.30x slower                                                  |
| raytrace                   | 253 ms                                                       | 329 ms: 1.30x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.2 ms: 1.31x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                 |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.58 ms: 1.47x slower                                                 |
| nbody                      | 85.1 ms                                                      | 136 ms: 1.60x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 94.3 ms: 8.58x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250122-3.14.0a4+-68ce740-NOGIL/bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.33x