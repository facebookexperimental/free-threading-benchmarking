# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: b0fcd85
- commit date: 2025-02-06
- overall geometric mean: 1.038x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 72.3 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 556 ms: 2.00x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                              |
| async_tree_io              | 1.08 sec                                               | 589 ms: 1.84x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                              |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                             |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.0 ms: 1.11x faster                                             |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                              |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                             |
| regex_compile  | 142 ms                                                 | 152 ms: 1.06x slower                                              |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                              |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 95.2 ms: 1.12x slower                                             |
| pickle_pure_python   | 308 us                                                 | 354 us: 1.15x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 68.0 ms: 1.15x slower                                             |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.77 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.7 ms: 1.17x slower                                             |
| django_template | 34.7 ms                                                | 41.4 ms: 1.19x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                             |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.67 ms: 2.07x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 556 ms: 2.00x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                              |
| async_tree_io              | 1.08 sec                                               | 589 ms: 1.84x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                              |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                             |
| deepcopy                   | 352 us                                                 | 304 us: 1.16x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                             |
| float                      | 80.8 ms                                                | 73.0 ms: 1.11x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.09x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 37.1 us: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                             |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                              |
| comprehensions             | 19.8 us                                                | 19.5 us: 1.02x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.65 sec: 1.02x faster                                            |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                              |
| scimark_sor                | 130 ms                                                 | 129 ms: 1.01x faster                                              |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.12 us: 1.01x slower                                             |
| raytrace                   | 299 ms                                                 | 310 ms: 1.04x slower                                              |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                             |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                            |
| regex_compile              | 142 ms                                                 | 152 ms: 1.06x slower                                              |
| chaos                      | 62.8 ms                                                | 67.1 ms: 1.07x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                             |
| logging_simple             | 6.63 us                                                | 7.14 us: 1.08x slower                                             |
| pyflate                    | 448 ms                                                 | 485 ms: 1.08x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                            |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                              |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 117 ms: 1.10x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.84 ms: 1.10x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                              |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                            |
| thrift                     | 791 us                                                 | 883 us: 1.12x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 95.2 ms: 1.12x slower                                             |
| logging_format             | 7.35 us                                                | 8.22 us: 1.12x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.52 ms: 1.12x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                             |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                             |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 60.4 ms: 1.13x slower                                             |
| html5lib                   | 63.6 ms                                                | 72.3 ms: 1.14x slower                                             |
| pickle_pure_python         | 308 us                                                 | 354 us: 1.15x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 88.1 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 68.0 ms: 1.15x slower                                             |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 58.7 ms: 1.17x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 81.2 ms: 1.19x slower                                             |
| sympy_expand               | 468 ms                                                 | 555 ms: 1.19x slower                                              |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                              |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.36 ms: 1.19x slower                                             |
| django_template            | 34.7 ms                                                | 41.4 ms: 1.19x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.2 ms: 1.20x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                             |
| richards                   | 45.9 ms                                                | 55.6 ms: 1.21x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                              |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                              |
| richards_super             | 51.9 ms                                                | 65.0 ms: 1.25x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                             |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                              |
| deltablue                  | 3.45 ms                                                | 4.55 ms: 1.32x slower                                             |
| telco                      | 6.53 ms                                                | 8.64 ms: 1.32x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.83 ms: 1.33x slower                                             |
| coverage                   | 71.4 ms                                                | 97.2 ms: 1.36x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.77 ms: 1.36x slower                                             |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.50x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.9 ms: 8.88x slower                                             |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (4): generators, asyncio_websockets, pylint, spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250206-3.14.0a4+-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.038x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x