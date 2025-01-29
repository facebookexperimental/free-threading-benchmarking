# Results vs. 3.12.6

- fork: Yhg1s
- ref: load_const_defer
- machine: linux-x86_64
- commit hash: fcfb942
- commit date: 2025-01-29
- overall geometric mean: 1.079x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 311 ms: 1.18x slower                                              |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                            |
| html5lib       | 63.6 ms                                                | 72.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 592 ms: 1.87x faster                                              |
| async_tree_io              | 1.08 sec                                               | 617 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                              |
| async_tree_none            | 464 ms                                                 | 295 ms: 1.58x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 360 ms: 1.54x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 629 ms: 1.14x faster                                              |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                              |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                             |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.1 ms: 1.03x faster                                             |
| pidigits       | 184 ms                                                 | 227 ms: 1.23x slower                                              |
| nbody          | 89.3 ms                                                | 143 ms: 1.60x slower                                              |
| Geometric mean | (ref)                                                  | 1.24x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                             |
| regex_compile  | 142 ms                                                 | 156 ms: 1.10x slower                                              |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.0 ms: 1.09x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| xml_etree_generate   | 85.2 ms                                                | 97.5 ms: 1.14x slower                                             |
| tomli_loads          | 2.11 sec                                               | 2.41 sec: 1.14x slower                                            |
| json_loads           | 26.5 us                                                | 30.9 us: 1.16x slower                                             |
| unpickle_pure_python | 221 us                                                 | 258 us: 1.17x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 70.0 ms: 1.19x slower                                             |
| pickle_pure_python   | 308 us                                                 | 383 us: 1.25x slower                                              |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.28x slower                                             |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                             |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                             |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.3 ms: 1.24x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.7 ms: 1.26x slower                                             |
| django_template | 34.7 ms                                                | 43.7 ms: 1.26x slower                                             |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 592 ms: 1.87x faster                                              |
| async_tree_io              | 1.08 sec                                               | 617 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                              |
| async_tree_none            | 464 ms                                                 | 295 ms: 1.58x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 360 ms: 1.54x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 629 ms: 1.14x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                             |
| deepcopy                   | 352 us                                                 | 320 us: 1.10x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 89.0 ms: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                             |
| float                      | 80.8 ms                                                | 78.1 ms: 1.03x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 39.1 us: 1.03x faster                                             |
| gc_traversal               | 3.46 ms                                                | 3.36 ms: 1.03x faster                                             |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.66 sec: 1.02x faster                                            |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                             |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                              |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.04x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.04x slower                                            |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                             |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                             |
| dulwich_log                | 78.9 ms                                                | 83.6 ms: 1.06x slower                                             |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                             |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                              |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.33 us: 1.08x slower                                             |
| regex_compile              | 142 ms                                                 | 156 ms: 1.10x slower                                              |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                            |
| pprint_safe_repr           | 743 ms                                                 | 830 ms: 1.12x slower                                              |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.13x slower                                             |
| logging_silent             | 109 ns                                                 | 123 ns: 1.13x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 162 ms: 1.13x slower                                              |
| chaos                      | 62.8 ms                                                | 71.2 ms: 1.13x slower                                             |
| pyflate                    | 448 ms                                                 | 507 ms: 1.13x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                            |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| html5lib                   | 63.6 ms                                                | 72.5 ms: 1.14x slower                                             |
| logging_simple             | 6.63 us                                                | 7.57 us: 1.14x slower                                             |
| raytrace                   | 299 ms                                                 | 342 ms: 1.14x slower                                              |
| sympy_sum                  | 166 ms                                                 | 190 ms: 1.14x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 97.5 ms: 1.14x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.41 sec: 1.14x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.15x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 88.9 ms: 1.16x slower                                             |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.16x slower                                             |
| scimark_fft                | 342 ms                                                 | 399 ms: 1.17x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 258 us: 1.17x slower                                              |
| sympy_str                  | 292 ms                                                 | 341 ms: 1.17x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 62.5 ms: 1.17x slower                                             |
| logging_format             | 7.35 us                                                | 8.63 us: 1.18x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.97 ms: 1.18x slower                                             |
| 2to3                       | 264 ms                                                 | 311 ms: 1.18x slower                                              |
| thrift                     | 791 us                                                 | 935 us: 1.18x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 70.0 ms: 1.19x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| sympy_expand               | 468 ms                                                 | 562 ms: 1.20x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.64 ms: 1.21x slower                                             |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.59 ms: 1.23x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                             |
| pidigits                   | 184 ms                                                 | 227 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.23x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 84.9 ms: 1.24x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 62.3 ms: 1.24x slower                                             |
| pickle_pure_python         | 308 us                                                 | 383 us: 1.25x slower                                              |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                              |
| genshi_text                | 22.8 ms                                                | 28.7 ms: 1.26x slower                                             |
| django_template            | 34.7 ms                                                | 43.7 ms: 1.26x slower                                             |
| richards                   | 45.9 ms                                                | 58.6 ms: 1.28x slower                                             |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.28x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                             |
| fannkuch                   | 372 ms                                                 | 488 ms: 1.31x slower                                              |
| richards_super             | 51.9 ms                                                | 69.0 ms: 1.33x slower                                             |
| telco                      | 6.53 ms                                                | 8.69 ms: 1.33x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                             |
| coverage                   | 71.4 ms                                                | 97.7 ms: 1.37x slower                                             |
| deltablue                  | 3.45 ms                                                | 4.79 ms: 1.39x slower                                             |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                             |
| nbody                      | 89.3 ms                                                | 143 ms: 1.60x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 94.9 ms: 8.79x slower                                             |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250129-3.14.0a4+-fcfb942-NOGIL/bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x