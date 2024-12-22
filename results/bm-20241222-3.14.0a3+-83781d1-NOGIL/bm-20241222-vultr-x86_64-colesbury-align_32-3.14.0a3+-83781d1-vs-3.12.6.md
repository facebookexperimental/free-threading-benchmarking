# Results vs. 3.12.6

- fork: colesbury
- ref: align_32
- machine: linux-x86_64
- commit hash: 83781d1
- commit date: 2024-12-22
- overall geometric mean: 1.177x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 357 ms: 1.36x slower                                          |
| docutils       | 2.64 sec                                               | 2.99 sec: 1.13x slower                                        |
| html5lib       | 63.6 ms                                                | 93.0 ms: 1.46x slower                                         |
| Geometric mean | (ref)                                                  | 1.31x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                          |
| async_tree_io              | 1.08 sec                                               | 766 ms: 1.41x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 406 ms: 1.38x faster                                          |
| async_tree_none            | 464 ms                                                 | 357 ms: 1.30x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 435 ms: 1.28x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 591 ms: 1.21x faster                                          |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                          |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                         |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                          |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                          |
| float          | 80.8 ms                                                | 109 ms: 1.35x slower                                          |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                          |
| Geometric mean | (ref)                                                  | 1.21x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                         |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                          |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                         |
| regex_compile  | 142 ms                                                 | 168 ms: 1.18x slower                                          |
| Geometric mean | (ref)                                                  | 1.03x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                         |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                          |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                         |
| xml_etree_generate   | 85.2 ms                                                | 97.8 ms: 1.15x slower                                         |
| tomli_loads          | 2.11 sec                                               | 2.47 sec: 1.17x slower                                        |
| xml_etree_process    | 59.0 ms                                                | 73.5 ms: 1.25x slower                                         |
| json_dumps           | 10.4 ms                                                | 13.3 ms: 1.29x slower                                         |
| unpickle_pure_python | 221 us                                                 | 327 us: 1.48x slower                                          |
| pickle_pure_python   | 308 us                                                 | 495 us: 1.61x slower                                          |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.1 ms: 1.41x slower                                         |
| python_startup         | 9.93 ms                                                | 17.0 ms: 1.71x slower                                         |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.0 ms: 1.27x slower                                         |
| genshi_text     | 22.8 ms                                                | 30.2 ms: 1.32x slower                                         |
| django_template | 34.7 ms                                                | 51.2 ms: 1.47x slower                                         |
| mako            | 11.0 ms                                                | 16.5 ms: 1.50x slower                                         |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                          |
| async_tree_io              | 1.08 sec                                               | 766 ms: 1.41x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 406 ms: 1.38x faster                                          |
| async_tree_none            | 464 ms                                                 | 357 ms: 1.30x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 435 ms: 1.28x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 591 ms: 1.21x faster                                          |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                         |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                         |
| deepcopy                   | 352 us                                                 | 326 us: 1.08x faster                                          |
| gc_traversal               | 3.46 ms                                                | 3.21 ms: 1.08x faster                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                         |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                          |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                         |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                          |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                          |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.02x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                          |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                         |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                         |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                         |
| scimark_fft                | 342 ms                                                 | 355 ms: 1.04x slower                                          |
| bpe_tokeniser              | 4.74 sec                                               | 4.97 sec: 1.05x slower                                        |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                          |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                         |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                        |
| deepcopy_reduce            | 3.08 us                                                | 3.46 us: 1.12x slower                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.97 ms: 1.13x slower                                         |
| docutils                   | 2.64 sec                                               | 2.99 sec: 1.13x slower                                        |
| generators                 | 32.2 ms                                                | 36.7 ms: 1.14x slower                                         |
| pylint                     | 319 ms                                                 | 364 ms: 1.14x slower                                          |
| xml_etree_generate         | 85.2 ms                                                | 97.8 ms: 1.15x slower                                         |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                          |
| crypto_pyaes               | 76.6 ms                                                | 89.3 ms: 1.17x slower                                         |
| tomli_loads                | 2.11 sec                                               | 2.47 sec: 1.17x slower                                        |
| dulwich_log                | 78.9 ms                                                | 92.5 ms: 1.17x slower                                         |
| regex_compile              | 142 ms                                                 | 168 ms: 1.18x slower                                          |
| pycparser                  | 1.17 sec                                               | 1.39 sec: 1.19x slower                                        |
| nqueens                    | 80.1 ms                                                | 98.3 ms: 1.23x slower                                         |
| sqlglot_optimize           | 53.3 ms                                                | 65.9 ms: 1.24x slower                                         |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.24x slower                                          |
| xml_etree_process          | 59.0 ms                                                | 73.5 ms: 1.25x slower                                         |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.27x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 64.0 ms: 1.27x slower                                         |
| thrift                     | 791 us                                                 | 1.01 ms: 1.28x slower                                         |
| json_dumps                 | 10.4 ms                                                | 13.3 ms: 1.29x slower                                         |
| pprint_safe_repr           | 743 ms                                                 | 959 ms: 1.29x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.4 ms: 1.30x slower                                         |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                        |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                          |
| genshi_text                | 22.8 ms                                                | 30.2 ms: 1.32x slower                                         |
| comprehensions             | 19.8 us                                                | 26.5 us: 1.33x slower                                         |
| float                      | 80.8 ms                                                | 109 ms: 1.35x slower                                          |
| telco                      | 6.53 ms                                                | 8.80 ms: 1.35x slower                                         |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                          |
| 2to3                       | 264 ms                                                 | 357 ms: 1.36x slower                                          |
| sqlalchemy_declarative     | 143 ms                                                 | 196 ms: 1.37x slower                                          |
| scimark_lu                 | 114 ms                                                 | 158 ms: 1.38x slower                                          |
| logging_simple             | 6.63 us                                                | 9.23 us: 1.39x slower                                         |
| coverage                   | 71.4 ms                                                | 100.0 ms: 1.40x slower                                        |
| logging_format             | 7.35 us                                                | 10.4 us: 1.41x slower                                         |
| python_startup_no_site     | 7.16 ms                                                | 10.1 ms: 1.41x slower                                         |
| richards_super             | 51.9 ms                                                | 73.8 ms: 1.42x slower                                         |
| pyflate                    | 448 ms                                                 | 637 ms: 1.42x slower                                          |
| richards                   | 45.9 ms                                                | 65.9 ms: 1.43x slower                                         |
| sympy_integrate            | 20.5 ms                                                | 29.7 ms: 1.45x slower                                         |
| html5lib                   | 63.6 ms                                                | 93.0 ms: 1.46x slower                                         |
| django_template            | 34.7 ms                                                | 51.2 ms: 1.47x slower                                         |
| unpickle_pure_python       | 221 us                                                 | 327 us: 1.48x slower                                          |
| chaos                      | 62.8 ms                                                | 93.6 ms: 1.49x slower                                         |
| mako                       | 11.0 ms                                                | 16.5 ms: 1.50x slower                                         |
| hexiom                     | 6.17 ms                                                | 9.37 ms: 1.52x slower                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 104 ms: 1.52x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.74 ms: 1.59x slower                                         |
| raytrace                   | 299 ms                                                 | 477 ms: 1.59x slower                                          |
| pickle_pure_python         | 308 us                                                 | 495 us: 1.61x slower                                          |
| sqlglot_transpile          | 1.67 ms                                                | 2.69 ms: 1.61x slower                                         |
| logging_silent             | 109 ns                                                 | 177 ns: 1.62x slower                                          |
| scimark_sor                | 130 ms                                                 | 211 ms: 1.63x slower                                          |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                          |
| go                         | 139 ms                                                 | 231 ms: 1.66x slower                                          |
| sqlglot_parse              | 1.36 ms                                                | 2.31 ms: 1.70x slower                                         |
| python_startup             | 9.93 ms                                                | 17.0 ms: 1.71x slower                                         |
| sympy_expand               | 468 ms                                                 | 957 ms: 2.05x slower                                          |
| deltablue                  | 3.45 ms                                                | 7.15 ms: 2.08x slower                                         |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                          |
| bench_thread_pool          | 941 us                                                 | 3.40 ms: 3.61x slower                                         |
| bench_mp_pool              | 10.8 ms                                                | 107 ms: 9.89x slower                                          |
| Geometric mean             | (ref)                                                  | 1.26x slower                                                  |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241222-3.14.0a3+-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.177x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.34x