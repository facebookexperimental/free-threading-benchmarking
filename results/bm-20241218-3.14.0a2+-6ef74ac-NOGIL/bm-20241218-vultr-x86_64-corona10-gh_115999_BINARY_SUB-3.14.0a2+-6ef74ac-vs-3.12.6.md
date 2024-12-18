# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.222x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| html5lib       | 63.6 ms                                                | 98.1 ms: 1.54x slower                                                    |
| Geometric mean | (ref)                                                  | 1.36x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 849 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 356 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 620 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 649 ms: 1.10x faster                                                     |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                    |
| async_generators           | 384 ms                                                 | 452 ms: 1.18x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                                     |
| float          | 80.8 ms                                                | 138 ms: 1.71x slower                                                     |
| Geometric mean | (ref)                                                  | 1.36x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.09x faster                                                    |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                     |
| regex_v8       | 20.6 ms                                                | 25.5 ms: 1.24x slower                                                    |
| regex_compile  | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 78.3 ms: 1.33x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 339 us: 1.54x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 516 us: 1.68x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                    |
| django_template | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                    |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 849 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 356 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 620 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 649 ms: 1.10x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.17 ms: 1.09x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.09x faster                                                    |
| deepcopy                   | 352 us                                                 | 329 us: 1.07x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| pathlib                    | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                    |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                     |
| spectral_norm              | 110 ms                                                 | 124 ms: 1.12x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.49 us: 1.14x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.15x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                    |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| async_generators           | 384 ms                                                 | 452 ms: 1.18x slower                                                     |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                    |
| pylint                     | 319 ms                                                 | 381 ms: 1.20x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 92.5 ms: 1.21x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 95.4 ms: 1.21x slower                                                    |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 25.5 ms: 1.24x slower                                                    |
| regex_compile              | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.68 ms: 1.29x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 68.9 ms: 1.29x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 964 ms: 1.30x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.53 sec: 1.31x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.32x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 78.3 ms: 1.33x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.3 ms: 1.35x slower                                                    |
| telco                      | 6.53 ms                                                | 8.81 ms: 1.35x slower                                                    |
| fannkuch                   | 372 ms                                                 | 504 ms: 1.35x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.35x slower                                                     |
| comprehensions             | 19.8 us                                                | 27.1 us: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| genshi_text                | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                    |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 203 ms: 1.42x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                                     |
| django_template            | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                    |
| thrift                     | 791 us                                                 | 1.16 ms: 1.47x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 339 us: 1.54x slower                                                     |
| html5lib                   | 63.6 ms                                                | 98.1 ms: 1.54x slower                                                    |
| pyflate                    | 448 ms                                                 | 693 ms: 1.55x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.75 ms: 1.58x slower                                                    |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| sympy_str                  | 292 ms                                                 | 475 ms: 1.63x slower                                                     |
| logging_simple             | 6.63 us                                                | 10.8 us: 1.63x slower                                                    |
| logging_format             | 7.35 us                                                | 12.1 us: 1.64x slower                                                    |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                    |
| richards                   | 45.9 ms                                                | 76.5 ms: 1.66x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 516 us: 1.68x slower                                                     |
| richards_super             | 51.9 ms                                                | 88.8 ms: 1.71x slower                                                    |
| float                      | 80.8 ms                                                | 138 ms: 1.71x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 118 ms: 1.72x slower                                                     |
| logging_silent             | 109 ns                                                 | 189 ns: 1.73x slower                                                     |
| scimark_sor                | 130 ms                                                 | 226 ms: 1.74x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 2.96 ms: 1.77x slower                                                    |
| raytrace                   | 299 ms                                                 | 549 ms: 1.83x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.55 ms: 1.88x slower                                                    |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                     |
| sympy_expand               | 468 ms                                                 | 953 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.02 ms: 2.33x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.64x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.07x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                             |

Benchmark hidden because not significant (4): deepcopy_memo, pidigits, asyncio_websockets, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241218-3.14.0a2+-6ef74ac-NOGIL/bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.222x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x