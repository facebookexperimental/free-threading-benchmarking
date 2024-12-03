# Results vs. 3.13.0rc2

- fork: python
- ref: 8ba9f5bca9c0ce6130e1
- machine: linux-x86_64
- commit hash: 8ba9f5b
- commit date: 2024-12-03
- overall geometric mean: 1.282x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 376 ms: 1.45x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                 |
| html5lib       | 67.0 ms                                                      | 100 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                        | 1.39x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 862 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                                   |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                                   |
| async_tree_none_tg        | 336 ms                                                       | 363 ms: 1.08x slower                                                   |
| async_tree_memoization_tg | 414 ms                                                       | 459 ms: 1.11x slower                                                   |
| async_tree_none           | 354 ms                                                       | 398 ms: 1.13x slower                                                   |
| coroutines                | 23.6 ms                                                      | 28.2 ms: 1.20x slower                                                  |
| async_generators          | 377 ms                                                       | 472 ms: 1.25x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| nbody          | 85.1 ms                                                      | 132 ms: 1.56x slower                                                   |
| float          | 77.5 ms                                                      | 143 ms: 1.84x slower                                                   |
| Geometric mean | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.5 ms: 1.12x slower                                                  |
| regex_compile  | 132 ms                                                       | 193 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 82.1 ms: 1.38x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.78 sec: 1.38x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 382 us: 1.82x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 570 us: 1.93x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 67.0 ms: 1.37x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 33.3 ms: 1.54x slower                                                  |
| django_template | 34.1 ms                                                      | 55.9 ms: 1.64x slower                                                  |
| mako            | 11.3 ms                                                      | 19.9 ms: 1.75x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.57x slower                                                           |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| async_tree_io_tg          | 913 ms                                                       | 862 ms: 1.06x faster                                                   |
| regex_effbot              | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                  |
| xml_etree_parse           | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                                   |
| json                      | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| json_loads                | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| sqlite_synth              | 2.21 us                                                      | 2.31 us: 1.05x slower                                                  |
| regex_dna                 | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| gc_traversal              | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                                  |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                                   |
| async_tree_none_tg        | 336 ms                                                       | 363 ms: 1.08x slower                                                   |
| pathlib                   | 19.2 ms                                                      | 20.9 ms: 1.09x slower                                                  |
| async_tree_memoization_tg | 414 ms                                                       | 459 ms: 1.11x slower                                                   |
| regex_v8                  | 22.7 ms                                                      | 25.5 ms: 1.12x slower                                                  |
| telco                     | 7.82 ms                                                      | 8.80 ms: 1.12x slower                                                  |
| async_tree_none           | 354 ms                                                       | 398 ms: 1.13x slower                                                   |
| deepcopy_memo             | 39.1 us                                                      | 45.1 us: 1.15x slower                                                  |
| scimark_fft               | 349 ms                                                       | 409 ms: 1.17x slower                                                   |
| spectral_norm             | 111 ms                                                       | 131 ms: 1.18x slower                                                   |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| coroutines                | 23.6 ms                                                      | 28.2 ms: 1.20x slower                                                  |
| deepcopy_reduce           | 3.11 us                                                      | 3.75 us: 1.20x slower                                                  |
| docutils                  | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                 |
| coverage                  | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| bpe_tokeniser             | 4.45 sec                                                     | 5.49 sec: 1.24x slower                                                 |
| pylint                    | 317 ms                                                       | 394 ms: 1.24x slower                                                   |
| async_generators          | 377 ms                                                       | 472 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.90 ms: 1.25x slower                                                  |
| mdp                       | 2.36 sec                                                     | 3.03 sec: 1.29x slower                                                 |
| nqueens                   | 78.6 ms                                                      | 103 ms: 1.31x slower                                                   |
| generators                | 28.8 ms                                                      | 38.1 ms: 1.32x slower                                                  |
| dulwich_log               | 74.8 ms                                                      | 99.1 ms: 1.32x slower                                                  |
| meteor_contest            | 102 ms                                                       | 135 ms: 1.33x slower                                                   |
| json_dumps                | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                  |
| create_gc_cycles          | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                  |
| genshi_xml                | 48.8 ms                                                      | 67.0 ms: 1.37x slower                                                  |
| typing_runtime_protocols  | 155 us                                                       | 213 us: 1.38x slower                                                   |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| xml_etree_process         | 59.3 ms                                                      | 82.1 ms: 1.38x slower                                                  |
| tomli_loads               | 2.01 sec                                                     | 2.78 sec: 1.38x slower                                                 |
| crypto_pyaes              | 67.9 ms                                                      | 94.3 ms: 1.39x slower                                                  |
| fannkuch                  | 370 ms                                                       | 515 ms: 1.39x slower                                                   |
| sqlglot_optimize          | 52.7 ms                                                      | 74.9 ms: 1.42x slower                                                  |
| sqlglot_normalize         | 106 ms                                                       | 150 ms: 1.42x slower                                                   |
| pycparser                 | 1.12 sec                                                     | 1.60 sec: 1.43x slower                                                 |
| pprint_safe_repr          | 738 ms                                                       | 1.06 sec: 1.44x slower                                                 |
| 2to3                      | 260 ms                                                       | 376 ms: 1.45x slower                                                   |
| regex_compile             | 132 ms                                                       | 193 ms: 1.46x slower                                                   |
| pprint_pformat            | 1.50 sec                                                     | 2.21 sec: 1.48x slower                                                 |
| html5lib                  | 67.0 ms                                                      | 100 ms: 1.50x slower                                                   |
| thrift                    | 778 us                                                       | 1.19 ms: 1.53x slower                                                  |
| genshi_text               | 21.5 ms                                                      | 33.3 ms: 1.54x slower                                                  |
| sympy_integrate           | 19.8 ms                                                      | 30.7 ms: 1.55x slower                                                  |
| nbody                     | 85.1 ms                                                      | 132 ms: 1.56x slower                                                   |
| python_startup            | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| pyflate                   | 449 ms                                                       | 734 ms: 1.64x slower                                                   |
| django_template           | 34.1 ms                                                      | 55.9 ms: 1.64x slower                                                  |
| scimark_lu                | 113 ms                                                       | 194 ms: 1.72x slower                                                   |
| mako                      | 11.3 ms                                                      | 19.9 ms: 1.75x slower                                                  |
| comprehensions            | 16.5 us                                                      | 29.2 us: 1.77x slower                                                  |
| sympy_str                 | 275 ms                                                       | 492 ms: 1.79x slower                                                   |
| logging_format            | 6.84 us                                                      | 12.3 us: 1.80x slower                                                  |
| scimark_sor               | 134 ms                                                       | 244 ms: 1.81x slower                                                   |
| unpickle_pure_python      | 210 us                                                       | 382 us: 1.82x slower                                                   |
| logging_simple            | 6.16 us                                                      | 11.2 us: 1.82x slower                                                  |
| hexiom                    | 5.99 ms                                                      | 10.9 ms: 1.82x slower                                                  |
| float                     | 77.5 ms                                                      | 143 ms: 1.84x slower                                                   |
| richards                  | 45.2 ms                                                      | 83.7 ms: 1.85x slower                                                  |
| scimark_monte_carlo       | 65.4 ms                                                      | 123 ms: 1.88x slower                                                   |
| pickle_pure_python        | 294 us                                                       | 570 us: 1.93x slower                                                   |
| chaos                     | 57.3 ms                                                      | 111 ms: 1.94x slower                                                   |
| richards_super            | 51.6 ms                                                      | 101 ms: 1.95x slower                                                   |
| sqlglot_transpile         | 1.56 ms                                                      | 3.06 ms: 1.96x slower                                                  |
| logging_silent            | 103 ns                                                       | 202 ns: 1.97x slower                                                   |
| go                        | 141 ms                                                       | 282 ms: 2.00x slower                                                   |
| sqlglot_parse             | 1.25 ms                                                      | 2.65 ms: 2.12x slower                                                  |
| sympy_expand              | 457 ms                                                       | 986 ms: 2.16x slower                                                   |
| sympy_sum                 | 156 ms                                                       | 357 ms: 2.29x slower                                                   |
| raytrace                  | 253 ms                                                       | 603 ms: 2.39x slower                                                   |
| deltablue                 | 3.12 ms                                                      | 8.82 ms: 2.82x slower                                                  |
| bench_thread_pool         | 919 us                                                       | 3.39 ms: 3.69x slower                                                  |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.97x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.44x slower                                                           |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, asyncio_websockets, deepcopy, xml_etree_iterparse, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-8ba9f5b-NOGIL/bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.282x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.31x