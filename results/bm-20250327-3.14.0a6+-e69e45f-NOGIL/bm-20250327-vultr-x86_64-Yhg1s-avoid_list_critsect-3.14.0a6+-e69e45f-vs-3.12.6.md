# Results vs. 3.12.6

- fork: Yhg1s
- ref: avoid_list_critsect
- machine: linux-x86_64
- commit hash: e69e45f
- commit date: 2025-03-27
- overall geometric mean: 1.050x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 299 ms: 1.14x slower                                                 |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                               |
| html5lib       | 63.6 ms                                                | 72.2 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                 |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 495 ms: 1.46x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 527 ms: 1.36x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                |
| async_generators           | 384 ms                                                 | 383 ms: 1.00x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                 |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                  | 1.15x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                 |
| regex_compile  | 142 ms                                                 | 159 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.40 sec: 1.14x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                |
| unpickle_pure_python | 221 us                                                 | 258 us: 1.17x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 363 us: 1.18x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.1 ms: 1.22x slower                                                |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                |
| django_template | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.90x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 301 ms: 1.86x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                 |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 495 ms: 1.46x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 527 ms: 1.36x faster                                                 |
| deepcopy                   | 352 us                                                 | 313 us: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.5 ms: 1.07x faster                                                |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                                |
| float                      | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                |
| async_generators           | 384 ms                                                 | 383 ms: 1.00x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.85 sec: 1.02x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.05x slower                                                 |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.32 ms: 1.06x slower                                                |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                |
| go                         | 139 ms                                                 | 148 ms: 1.06x slower                                                 |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.06x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                               |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                |
| thrift                     | 791 us                                                 | 869 us: 1.10x slower                                                 |
| raytrace                   | 299 ms                                                 | 329 ms: 1.10x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.32 us: 1.10x slower                                                |
| chaos                      | 62.8 ms                                                | 69.5 ms: 1.11x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                 |
| regex_compile              | 142 ms                                                 | 159 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                 |
| pyflate                    | 448 ms                                                 | 506 ms: 1.13x slower                                                 |
| html5lib                   | 63.6 ms                                                | 72.2 ms: 1.13x slower                                                |
| logging_format             | 7.35 us                                                | 8.34 us: 1.14x slower                                                |
| 2to3                       | 264 ms                                                 | 299 ms: 1.14x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.40 sec: 1.14x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.95 ms: 1.15x slower                                                |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 855 ms: 1.15x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                                |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                               |
| scimark_fft                | 342 ms                                                 | 395 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.78 sec: 1.17x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 258 us: 1.17x slower                                                 |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 363 us: 1.18x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 61.1 ms: 1.22x slower                                                |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                                |
| richards                   | 45.9 ms                                                | 56.2 ms: 1.22x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 84.6 ms: 1.24x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                |
| hexiom                     | 6.17 ms                                                | 7.71 ms: 1.25x slower                                                |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                |
| richards_super             | 51.9 ms                                                | 65.1 ms: 1.25x slower                                                |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.26x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                                |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                 |
| django_template            | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.64 ms: 1.28x slower                                                |
| fannkuch                   | 372 ms                                                 | 498 ms: 1.34x slower                                                 |
| telco                      | 6.53 ms                                                | 9.04 ms: 1.38x slower                                                |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                 |
| coverage                   | 71.4 ms                                                | 109 ms: 1.53x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 97.1 ms: 8.99x slower                                                |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                         |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250327-3.14.0a6+-e69e45f-NOGIL/bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x