# Results vs. 3.12.6

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.218x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 364 ms: 1.38x slower                                        |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                      |
| html5lib       | 63.6 ms                                                | 95.2 ms: 1.50x slower                                       |
| Geometric mean | (ref)                                                  | 1.34x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 818 ms: 1.36x faster                                        |
| async_tree_io              | 1.08 sec                                               | 843 ms: 1.28x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 449 ms: 1.25x faster                                        |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 470 ms: 1.18x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 615 ms: 1.17x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 635 ms: 1.13x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                        |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                       |
| async_generators           | 384 ms                                                 | 462 ms: 1.20x slower                                        |
| Geometric mean             | (ref)                                                  | 1.14x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                        |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                        |
| float          | 80.8 ms                                                | 138 ms: 1.71x slower                                        |
| Geometric mean | (ref)                                                  | 1.35x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                       |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                        |
| regex_v8       | 20.6 ms                                                | 24.3 ms: 1.18x slower                                       |
| regex_compile  | 142 ms                                                 | 179 ms: 1.26x slower                                        |
| Geometric mean | (ref)                                                  | 1.09x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.3 ms: 1.07x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                        |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                       |
| xml_etree_generate   | 85.2 ms                                                | 98.9 ms: 1.16x slower                                       |
| tomli_loads          | 2.11 sec                                               | 2.47 sec: 1.17x slower                                      |
| xml_etree_process    | 59.0 ms                                                | 78.6 ms: 1.33x slower                                       |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                       |
| unpickle_pure_python | 221 us                                                 | 329 us: 1.49x slower                                        |
| pickle_pure_python   | 308 us                                                 | 497 us: 1.61x slower                                        |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                       |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                       |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.3 ms: 1.28x slower                                       |
| genshi_text     | 22.8 ms                                                | 31.4 ms: 1.38x slower                                       |
| django_template | 34.7 ms                                                | 50.1 ms: 1.45x slower                                       |
| mako            | 11.0 ms                                                | 17.7 ms: 1.61x slower                                       |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 818 ms: 1.36x faster                                        |
| async_tree_io              | 1.08 sec                                               | 843 ms: 1.28x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 449 ms: 1.25x faster                                        |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 470 ms: 1.18x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 615 ms: 1.17x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 635 ms: 1.13x faster                                        |
| gc_traversal               | 3.46 ms                                                | 3.18 ms: 1.09x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 90.3 ms: 1.07x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                        |
| deepcopy                   | 352 us                                                 | 331 us: 1.06x faster                                        |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                       |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                        |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                       |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                       |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.94 sec: 1.04x slower                                      |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                        |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                       |
| spectral_norm              | 110 ms                                                 | 122 ms: 1.11x slower                                        |
| mdp                        | 2.42 sec                                               | 2.76 sec: 1.14x slower                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.51 us: 1.14x slower                                       |
| scimark_fft                | 342 ms                                                 | 396 ms: 1.16x slower                                        |
| xml_etree_generate         | 85.2 ms                                                | 98.9 ms: 1.16x slower                                       |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                      |
| tomli_loads                | 2.11 sec                                               | 2.47 sec: 1.17x slower                                      |
| regex_v8                   | 20.6 ms                                                | 24.3 ms: 1.18x slower                                       |
| crypto_pyaes               | 76.6 ms                                                | 91.2 ms: 1.19x slower                                       |
| pylint                     | 319 ms                                                 | 380 ms: 1.19x slower                                        |
| async_generators           | 384 ms                                                 | 462 ms: 1.20x slower                                        |
| dulwich_log                | 78.9 ms                                                | 95.1 ms: 1.21x slower                                       |
| nqueens                    | 80.1 ms                                                | 96.9 ms: 1.21x slower                                       |
| generators                 | 32.2 ms                                                | 39.3 ms: 1.22x slower                                       |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.23x slower                                        |
| regex_compile              | 142 ms                                                 | 179 ms: 1.26x slower                                        |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.27x slower                                        |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                        |
| genshi_xml                 | 50.2 ms                                                | 64.3 ms: 1.28x slower                                       |
| fannkuch                   | 372 ms                                                 | 479 ms: 1.29x slower                                        |
| sqlglot_optimize           | 53.3 ms                                                | 68.7 ms: 1.29x slower                                       |
| pycparser                  | 1.17 sec                                               | 1.51 sec: 1.30x slower                                      |
| pprint_safe_repr           | 743 ms                                                 | 970 ms: 1.31x slower                                        |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                      |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 78.6 ms: 1.33x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.88 ms: 1.34x slower                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.4 ms: 1.35x slower                                       |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                       |
| comprehensions             | 19.8 us                                                | 27.1 us: 1.37x slower                                       |
| coverage                   | 71.4 ms                                                | 98.2 ms: 1.38x slower                                       |
| genshi_text                | 22.8 ms                                                | 31.4 ms: 1.38x slower                                       |
| 2to3                       | 264 ms                                                 | 364 ms: 1.38x slower                                        |
| sympy_integrate            | 20.5 ms                                                | 29.2 ms: 1.42x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 203 ms: 1.42x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                       |
| django_template            | 34.7 ms                                                | 50.1 ms: 1.45x slower                                       |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                        |
| thrift                     | 791 us                                                 | 1.16 ms: 1.47x slower                                       |
| pyflate                    | 448 ms                                                 | 666 ms: 1.49x slower                                        |
| unpickle_pure_python       | 221 us                                                 | 329 us: 1.49x slower                                        |
| html5lib                   | 63.6 ms                                                | 95.2 ms: 1.50x slower                                       |
| hexiom                     | 6.17 ms                                                | 9.55 ms: 1.55x slower                                       |
| logging_format             | 7.35 us                                                | 11.7 us: 1.59x slower                                       |
| mako                       | 11.0 ms                                                | 17.7 ms: 1.61x slower                                       |
| logging_simple             | 6.63 us                                                | 10.7 us: 1.61x slower                                       |
| pickle_pure_python         | 308 us                                                 | 497 us: 1.61x slower                                        |
| sympy_str                  | 292 ms                                                 | 472 ms: 1.62x slower                                        |
| scimark_lu                 | 114 ms                                                 | 186 ms: 1.63x slower                                        |
| chaos                      | 62.8 ms                                                | 104 ms: 1.66x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 116 ms: 1.69x slower                                        |
| richards                   | 45.9 ms                                                | 78.2 ms: 1.70x slower                                       |
| richards_super             | 51.9 ms                                                | 88.5 ms: 1.71x slower                                       |
| scimark_sor                | 130 ms                                                 | 221 ms: 1.71x slower                                        |
| float                      | 80.8 ms                                                | 138 ms: 1.71x slower                                        |
| logging_silent             | 109 ns                                                 | 188 ns: 1.73x slower                                        |
| sqlglot_transpile          | 1.67 ms                                                | 2.91 ms: 1.74x slower                                       |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                       |
| sqlglot_parse              | 1.36 ms                                                | 2.52 ms: 1.86x slower                                       |
| raytrace                   | 299 ms                                                 | 559 ms: 1.87x slower                                        |
| go                         | 139 ms                                                 | 266 ms: 1.91x slower                                        |
| sympy_expand               | 468 ms                                                 | 945 ms: 2.02x slower                                        |
| sympy_sum                  | 166 ms                                                 | 349 ms: 2.10x slower                                        |
| deltablue                  | 3.45 ms                                                | 8.06 ms: 2.34x slower                                       |
| bench_thread_pool          | 941 us                                                 | 3.40 ms: 3.61x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241211-3.14.0a2+-47785d8-NOGIL/bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.218x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x