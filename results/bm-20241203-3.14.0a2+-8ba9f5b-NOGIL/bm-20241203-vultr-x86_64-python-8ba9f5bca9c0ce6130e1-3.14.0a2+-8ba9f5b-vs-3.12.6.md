# Results vs. 3.12.6

- fork: python
- ref: 8ba9f5bca9c0ce6130e1
- machine: linux-x86_64
- commit hash: 8ba9f5b
- commit date: 2024-12-03
- overall geometric mean: 1.257x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 376 ms: 1.43x slower                                                   |
| docutils       | 2.64 sec                                               | 3.21 sec: 1.22x slower                                                 |
| html5lib       | 63.6 ms                                                | 100 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                  | 1.40x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 862 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 887 ms: 1.22x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 459 ms: 1.22x faster                                                   |
| async_tree_none            | 464 ms                                                 | 398 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.2 ms: 1.18x slower                                                  |
| async_generators           | 384 ms                                                 | 472 ms: 1.23x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                   |
| float          | 80.8 ms                                                | 143 ms: 1.77x slower                                                   |
| Geometric mean | (ref)                                                  | 1.38x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.5 ms: 1.24x slower                                                  |
| regex_compile  | 142 ms                                                 | 193 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.78 sec: 1.32x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 82.1 ms: 1.39x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 382 us: 1.73x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 570 us: 1.85x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 67.0 ms: 1.34x slower                                                  |
| genshi_text     | 22.8 ms                                                | 33.3 ms: 1.46x slower                                                  |
| django_template | 34.7 ms                                                | 55.9 ms: 1.61x slower                                                  |
| mako            | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.54x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 862 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 887 ms: 1.22x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 459 ms: 1.22x faster                                                   |
| async_tree_none            | 464 ms                                                 | 398 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.9 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| deepcopy                   | 352 us                                                 | 356 us: 1.01x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| deepcopy_memo              | 40.3 us                                                | 45.1 us: 1.12x slower                                                  |
| regex_dna                  | 168 ms                                                 | 189 ms: 1.13x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.49 sec: 1.16x slower                                                 |
| coroutines                 | 23.9 ms                                                | 28.2 ms: 1.18x slower                                                  |
| generators                 | 32.2 ms                                                | 38.1 ms: 1.18x slower                                                  |
| spectral_norm              | 110 ms                                                 | 131 ms: 1.19x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| scimark_fft                | 342 ms                                                 | 409 ms: 1.20x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.21 sec: 1.22x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.75 us: 1.22x slower                                                  |
| async_generators           | 384 ms                                                 | 472 ms: 1.23x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 94.3 ms: 1.23x slower                                                  |
| pylint                     | 319 ms                                                 | 394 ms: 1.24x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 25.5 ms: 1.24x slower                                                  |
| mdp                        | 2.42 sec                                               | 3.03 sec: 1.25x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 99.1 ms: 1.26x slower                                                  |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.28x slower                                                   |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.30x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 213 us: 1.31x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.78 sec: 1.32x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 67.0 ms: 1.34x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.90 ms: 1.34x slower                                                  |
| telco                      | 6.53 ms                                                | 8.80 ms: 1.35x slower                                                  |
| regex_compile              | 142 ms                                                 | 193 ms: 1.35x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.60 sec: 1.37x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.0 ms: 1.38x slower                                                  |
| fannkuch                   | 372 ms                                                 | 515 ms: 1.38x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 82.1 ms: 1.39x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 74.9 ms: 1.41x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 150 ms: 1.41x slower                                                   |
| 2to3                       | 264 ms                                                 | 376 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 1.06 sec: 1.43x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 207 ms: 1.45x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.21 sec: 1.45x slower                                                 |
| genshi_text                | 22.8 ms                                                | 33.3 ms: 1.46x slower                                                  |
| comprehensions             | 19.8 us                                                | 29.2 us: 1.47x slower                                                  |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 30.7 ms: 1.50x slower                                                  |
| thrift                     | 791 us                                                 | 1.19 ms: 1.51x slower                                                  |
| html5lib                   | 63.6 ms                                                | 100 ms: 1.58x slower                                                   |
| django_template            | 34.7 ms                                                | 55.9 ms: 1.61x slower                                                  |
| pyflate                    | 448 ms                                                 | 734 ms: 1.64x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                                  |
| logging_format             | 7.35 us                                                | 12.3 us: 1.68x slower                                                  |
| sympy_str                  | 292 ms                                                 | 492 ms: 1.69x slower                                                   |
| logging_simple             | 6.63 us                                                | 11.2 us: 1.69x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 194 ms: 1.70x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 382 us: 1.73x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                  |
| float                      | 80.8 ms                                                | 143 ms: 1.77x slower                                                   |
| hexiom                     | 6.17 ms                                                | 10.9 ms: 1.77x slower                                                  |
| chaos                      | 62.8 ms                                                | 111 ms: 1.77x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.80x slower                                                   |
| mako                       | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                  |
| richards                   | 45.9 ms                                                | 83.7 ms: 1.82x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.06 ms: 1.83x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 570 us: 1.85x slower                                                   |
| logging_silent             | 109 ns                                                 | 202 ns: 1.85x slower                                                   |
| scimark_sor                | 130 ms                                                 | 244 ms: 1.88x slower                                                   |
| richards_super             | 51.9 ms                                                | 101 ms: 1.94x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.65 ms: 1.96x slower                                                  |
| raytrace                   | 299 ms                                                 | 603 ms: 2.01x slower                                                   |
| go                         | 139 ms                                                 | 282 ms: 2.02x slower                                                   |
| sympy_expand               | 468 ms                                                 | 986 ms: 2.11x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.82 ms: 2.56x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.40x slower                                                           |

Benchmark hidden because not significant (2): pidigits, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-8ba9f5b-NOGIL/bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.257x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.33x