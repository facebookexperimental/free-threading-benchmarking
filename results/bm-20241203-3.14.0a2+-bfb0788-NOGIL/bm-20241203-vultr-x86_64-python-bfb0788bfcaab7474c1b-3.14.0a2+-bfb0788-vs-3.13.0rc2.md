# Results vs. 3.13.0rc2

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.283x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 377 ms: 1.45x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                                 |
| html5lib       | 67.0 ms                                                      | 102 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                        | 1.40x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 862 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 624 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 654 ms: 1.02x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 493 ms: 1.07x slower                                                   |
| async_tree_none_tg         | 336 ms                                                       | 368 ms: 1.09x slower                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 462 ms: 1.12x slower                                                   |
| async_tree_none            | 354 ms                                                       | 400 ms: 1.13x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                                  |
| async_generators           | 377 ms                                                       | 471 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| nbody          | 85.1 ms                                                      | 134 ms: 1.57x slower                                                   |
| float          | 77.5 ms                                                      | 142 ms: 1.83x slower                                                   |
| Geometric mean | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                  |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 26.1 ms: 1.15x slower                                                  |
| regex_compile  | 132 ms                                                       | 194 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.77 sec: 1.38x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 386 us: 1.84x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 562 us: 1.91x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 67.6 ms: 1.39x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 33.6 ms: 1.56x slower                                                  |
| django_template | 34.1 ms                                                      | 55.6 ms: 1.63x slower                                                  |
| mako            | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 862 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 624 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 654 ms: 1.02x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                  |
| deepcopy                   | 355 us                                                       | 354 us: 1.00x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.19 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.04x slower                                                  |
| async_tree_memoization     | 461 ms                                                       | 493 ms: 1.07x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 20.6 ms: 1.07x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 368 ms: 1.09x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.73 ms: 1.12x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 462 ms: 1.12x slower                                                   |
| async_tree_none            | 354 ms                                                       | 400 ms: 1.13x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 26.1 ms: 1.15x slower                                                  |
| scimark_fft                | 349 ms                                                       | 408 ms: 1.17x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 45.8 us: 1.17x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| spectral_norm              | 111 ms                                                       | 132 ms: 1.19x slower                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.74 us: 1.20x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                                  |
| coverage                   | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 5.51 sec: 1.24x slower                                                 |
| pylint                     | 317 ms                                                       | 395 ms: 1.25x slower                                                   |
| async_generators           | 377 ms                                                       | 471 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.90 ms: 1.25x slower                                                  |
| mdp                        | 2.36 sec                                                     | 3.03 sec: 1.28x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 103 ms: 1.31x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 98.7 ms: 1.32x slower                                                  |
| meteor_contest             | 102 ms                                                       | 135 ms: 1.33x slower                                                   |
| generators                 | 28.8 ms                                                      | 39.1 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 213 us: 1.38x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 93.8 ms: 1.38x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.77 sec: 1.38x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 67.6 ms: 1.39x slower                                                  |
| fannkuch                   | 370 ms                                                       | 517 ms: 1.40x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 150 ms: 1.41x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 74.7 ms: 1.42x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.61 sec: 1.44x slower                                                 |
| 2to3                       | 260 ms                                                       | 377 ms: 1.45x slower                                                   |
| regex_compile              | 132 ms                                                       | 194 ms: 1.46x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 1.08 sec: 1.47x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 2.24 sec: 1.49x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 102 ms: 1.52x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 30.7 ms: 1.55x slower                                                  |
| thrift                     | 778 us                                                       | 1.21 ms: 1.55x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 33.6 ms: 1.56x slower                                                  |
| nbody                      | 85.1 ms                                                      | 134 ms: 1.57x slower                                                   |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| django_template            | 34.1 ms                                                      | 55.6 ms: 1.63x slower                                                  |
| pyflate                    | 449 ms                                                       | 737 ms: 1.64x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 193 ms: 1.71x slower                                                   |
| mako                       | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                  |
| comprehensions             | 16.5 us                                                      | 29.2 us: 1.77x slower                                                  |
| sympy_str                  | 275 ms                                                       | 492 ms: 1.79x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 10.8 ms: 1.79x slower                                                  |
| scimark_sor                | 134 ms                                                       | 243 ms: 1.81x slower                                                   |
| logging_format             | 6.84 us                                                      | 12.5 us: 1.82x slower                                                  |
| logging_simple             | 6.16 us                                                      | 11.2 us: 1.82x slower                                                  |
| float                      | 77.5 ms                                                      | 142 ms: 1.83x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 386 us: 1.84x slower                                                   |
| richards                   | 45.2 ms                                                      | 84.0 ms: 1.86x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 123 ms: 1.88x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 562 us: 1.91x slower                                                   |
| chaos                      | 57.3 ms                                                      | 112 ms: 1.96x slower                                                   |
| richards_super             | 51.6 ms                                                      | 101 ms: 1.96x slower                                                   |
| logging_silent             | 103 ns                                                       | 201 ns: 1.96x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 3.06 ms: 1.96x slower                                                  |
| go                         | 141 ms                                                       | 283 ms: 2.01x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.64 ms: 2.12x slower                                                  |
| sympy_expand               | 457 ms                                                       | 986 ms: 2.16x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 357 ms: 2.29x slower                                                   |
| raytrace                   | 253 ms                                                       | 611 ms: 2.42x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 8.78 ms: 2.81x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 110 ms: 9.96x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.45x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_iterparse, asyncio_websockets, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.283x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.31x