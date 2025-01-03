# Results vs. 3.12.6

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.167x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 351 ms: 1.33x slower                                                   |
| docutils       | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                 |
| html5lib       | 63.6 ms                                                | 93.4 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 719 ms: 1.54x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 309 ms: 1.45x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 749 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                   |
| async_tree_none            | 464 ms                                                 | 348 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 422 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| float          | 80.8 ms                                                | 108 ms: 1.34x slower                                                   |
| nbody          | 89.3 ms                                                | 129 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.5 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.55 sec: 1.21x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 74.0 ms: 1.26x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 327 us: 1.48x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 499 us: 1.62x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.9 ms: 1.27x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                  |
| django_template | 34.7 ms                                                | 49.6 ms: 1.43x slower                                                  |
| mako            | 11.0 ms                                                | 17.2 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 719 ms: 1.54x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 309 ms: 1.45x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 749 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                   |
| async_tree_none            | 464 ms                                                 | 348 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 422 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                  |
| deepcopy                   | 352 us                                                 | 324 us: 1.09x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 89.5 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.11 us: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.8 us: 1.01x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.07x slower                                                 |
| pylint                     | 319 ms                                                 | 347 ms: 1.09x slower                                                   |
| scimark_fft                | 342 ms                                                 | 377 ms: 1.10x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.40 us: 1.10x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 90.0 ms: 1.14x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.37 sec: 1.17x slower                                                 |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 90.1 ms: 1.18x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.18x slower                                                   |
| generators                 | 32.2 ms                                                | 38.3 ms: 1.19x slower                                                  |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.55 sec: 1.21x slower                                                 |
| sympy_str                  | 292 ms                                                 | 355 ms: 1.22x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.9 ms: 1.22x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 25.2 ms: 1.23x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.24x slower                                                   |
| sympy_expand               | 468 ms                                                 | 584 ms: 1.25x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.3 ms: 1.25x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 66.6 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 74.0 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 207 us: 1.26x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 943 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.58 ms: 1.27x slower                                                  |
| thrift                     | 791 us                                                 | 1.01 ms: 1.27x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.9 ms: 1.27x slower                                                  |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.28x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.28x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.97 sec: 1.30x slower                                                 |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                                  |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                                   |
| 2to3                       | 264 ms                                                 | 351 ms: 1.33x slower                                                   |
| float                      | 80.8 ms                                                | 108 ms: 1.34x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.36x slower                                                   |
| genshi_text                | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                  |
| logging_simple             | 6.63 us                                                | 9.10 us: 1.37x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.7 ms: 1.38x slower                                                  |
| logging_format             | 7.35 us                                                | 10.3 us: 1.41x slower                                                  |
| django_template            | 34.7 ms                                                | 49.6 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 129 ms: 1.45x slower                                                   |
| html5lib                   | 63.6 ms                                                | 93.4 ms: 1.47x slower                                                  |
| richards                   | 45.9 ms                                                | 67.6 ms: 1.47x slower                                                  |
| richards_super             | 51.9 ms                                                | 76.5 ms: 1.47x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 327 us: 1.48x slower                                                   |
| pyflate                    | 448 ms                                                 | 665 ms: 1.48x slower                                                   |
| chaos                      | 62.8 ms                                                | 96.0 ms: 1.53x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.55x slower                                                   |
| hexiom                     | 6.17 ms                                                | 9.62 ms: 1.56x slower                                                  |
| mako                       | 11.0 ms                                                | 17.2 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.69 ms: 1.61x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 499 us: 1.62x slower                                                   |
| raytrace                   | 299 ms                                                 | 489 ms: 1.64x slower                                                   |
| scimark_sor                | 130 ms                                                 | 216 ms: 1.66x slower                                                   |
| logging_silent             | 109 ns                                                 | 181 ns: 1.66x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                  |
| go                         | 139 ms                                                 | 238 ms: 1.71x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.32 ms: 1.72x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.39 ms: 2.14x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.37 ms: 3.58x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.27x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.167x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.33x