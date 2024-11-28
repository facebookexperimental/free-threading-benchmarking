# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.258x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 377 ms: 1.43x slower                                                     |
| docutils       | 2.64 sec                                               | 3.19 sec: 1.21x slower                                                   |
| html5lib       | 63.6 ms                                                | 101 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                  | 1.40x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 864 ms: 1.28x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 367 ms: 1.22x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 893 ms: 1.21x faster                                                     |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 657 ms: 1.09x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 28.2 ms: 1.18x slower                                                    |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 89.3 ms                                                | 139 ms: 1.56x slower                                                     |
| float          | 80.8 ms                                                | 144 ms: 1.78x slower                                                     |
| Geometric mean | (ref)                                                  | 1.40x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| regex_dna      | 168 ms                                                 | 187 ms: 1.12x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| regex_compile  | 142 ms                                                 | 194 ms: 1.36x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.75 sec: 1.31x slower                                                   |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 378 us: 1.71x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 549 us: 1.78x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 67.2 ms: 1.34x slower                                                    |
| genshi_text     | 22.8 ms                                                | 33.6 ms: 1.47x slower                                                    |
| django_template | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                    |
| mako            | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.54x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 864 ms: 1.28x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 367 ms: 1.22x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 893 ms: 1.21x faster                                                     |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 657 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                    |
| pathlib                    | 21.5 ms                                                | 20.8 ms: 1.03x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                    |
| deepcopy                   | 352 us                                                 | 356 us: 1.01x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                                    |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.12x slower                                                     |
| deepcopy_memo              | 40.3 us                                                | 45.9 us: 1.14x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.55 sec: 1.17x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.2 ms: 1.18x slower                                                    |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.91 sec: 1.20x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.19 sec: 1.21x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.76 us: 1.22x slower                                                    |
| generators                 | 32.2 ms                                                | 39.4 ms: 1.22x slower                                                    |
| spectral_norm              | 110 ms                                                 | 135 ms: 1.23x slower                                                     |
| pylint                     | 319 ms                                                 | 394 ms: 1.24x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 99.8 ms: 1.27x slower                                                    |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.28x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 98.6 ms: 1.29x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.75 sec: 1.31x slower                                                   |
| meteor_contest             | 104 ms                                                 | 136 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 217 us: 1.33x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 67.2 ms: 1.34x slower                                                    |
| regex_compile              | 142 ms                                                 | 194 ms: 1.36x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.99 ms: 1.36x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.60 sec: 1.37x slower                                                   |
| telco                      | 6.53 ms                                                | 8.95 ms: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| fannkuch                   | 372 ms                                                 | 521 ms: 1.40x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 75.0 ms: 1.41x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 150 ms: 1.41x slower                                                     |
| 2to3                       | 264 ms                                                 | 377 ms: 1.43x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 1.07 sec: 1.44x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.22 sec: 1.46x slower                                                   |
| genshi_text                | 22.8 ms                                                | 33.6 ms: 1.47x slower                                                    |
| comprehensions             | 19.8 us                                                | 29.2 us: 1.47x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 30.9 ms: 1.51x slower                                                    |
| thrift                     | 791 us                                                 | 1.20 ms: 1.51x slower                                                    |
| nbody                      | 89.3 ms                                                | 139 ms: 1.56x slower                                                     |
| html5lib                   | 63.6 ms                                                | 101 ms: 1.58x slower                                                     |
| django_template            | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                    |
| pyflate                    | 448 ms                                                 | 741 ms: 1.65x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                    |
| sympy_str                  | 292 ms                                                 | 495 ms: 1.70x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 195 ms: 1.71x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 378 us: 1.71x slower                                                     |
| logging_format             | 7.35 us                                                | 12.6 us: 1.72x slower                                                    |
| logging_simple             | 6.63 us                                                | 11.4 us: 1.72x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 121 ms: 1.77x slower                                                     |
| chaos                      | 62.8 ms                                                | 112 ms: 1.78x slower                                                     |
| float                      | 80.8 ms                                                | 144 ms: 1.78x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 549 us: 1.78x slower                                                     |
| hexiom                     | 6.17 ms                                                | 11.0 ms: 1.79x slower                                                    |
| mako                       | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                    |
| richards                   | 45.9 ms                                                | 83.6 ms: 1.82x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.04 ms: 1.82x slower                                                    |
| logging_silent             | 109 ns                                                 | 200 ns: 1.83x slower                                                     |
| scimark_sor                | 130 ms                                                 | 242 ms: 1.86x slower                                                     |
| richards_super             | 51.9 ms                                                | 99.7 ms: 1.92x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.69 ms: 1.98x slower                                                    |
| raytrace                   | 299 ms                                                 | 599 ms: 2.00x slower                                                     |
| go                         | 139 ms                                                 | 281 ms: 2.01x slower                                                     |
| sympy_expand               | 468 ms                                                 | 982 ms: 2.10x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.80 ms: 2.55x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.40x slower                                                             |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241128-3.14.0a2+-6e2f5fe-NOGIL/bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.258x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x