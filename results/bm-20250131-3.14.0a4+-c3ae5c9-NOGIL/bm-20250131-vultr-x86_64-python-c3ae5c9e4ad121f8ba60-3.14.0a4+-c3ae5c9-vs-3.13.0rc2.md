# Results vs. 3.13.0rc2

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.061x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 295 ms: 1.14x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                 |
| html5lib       | 67.0 ms                                                      | 69.2 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 561 ms: 1.63x faster                                                   |
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 548 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 582 ms: 1.14x faster                                                   |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| float          | 77.5 ms                                                      | 74.4 ms: 1.04x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| regex_compile  | 132 ms                                                       | 145 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.4 ms: 1.10x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 94.5 ms: 1.11x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 67.1 ms: 1.13x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 240 us: 1.14x slower                                                   |
| json_loads           | 27.0 us                                                      | 31.5 us: 1.17x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.7 ms: 1.20x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 360 us: 1.22x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 56.4 ms: 1.16x slower                                                  |
| django_template | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                  |
| mako            | 11.3 ms                                                      | 15.3 ms: 1.35x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.73 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 561 ms: 1.63x faster                                                   |
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                                   |
| deepcopy                   | 355 us                                                       | 301 us: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 548 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 582 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.4 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.01 us: 1.10x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                  |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 36.9 us: 1.06x faster                                                  |
| go                         | 141 ms                                                       | 133 ms: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                  |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                   |
| scimark_sor                | 134 ms                                                       | 129 ms: 1.04x faster                                                   |
| float                      | 77.5 ms                                                      | 74.4 ms: 1.04x faster                                                  |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.09 us: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.03x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.57 sec: 1.03x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 69.2 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.03x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                 |
| logging_silent             | 103 ns                                                       | 108 ns: 1.05x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 783 ms: 1.06x slower                                                   |
| generators                 | 28.8 ms                                                      | 30.6 ms: 1.06x slower                                                  |
| scimark_fft                | 349 ms                                                       | 372 ms: 1.06x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.08x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 80.9 ms: 1.08x slower                                                  |
| pyflate                    | 449 ms                                                       | 486 ms: 1.08x slower                                                   |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                                  |
| regex_compile              | 132 ms                                                       | 145 ms: 1.10x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.62 ms: 1.10x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 94.5 ms: 1.11x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.61 sec: 1.11x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 118 ms: 1.11x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 67.1 ms: 1.13x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                 |
| 2to3                       | 260 ms                                                       | 295 ms: 1.14x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 60.0 ms: 1.14x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.01 us: 1.14x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 240 us: 1.14x slower                                                   |
| coverage                   | 83.0 ms                                                      | 95.2 ms: 1.15x slower                                                  |
| thrift                     | 778 us                                                       | 897 us: 1.15x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.89 us: 1.15x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 56.4 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.45 ms: 1.16x slower                                                  |
| chaos                      | 57.3 ms                                                      | 66.4 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.17x slower                                                   |
| comprehensions             | 16.5 us                                                      | 19.4 us: 1.18x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 184 ms: 1.18x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 7.10 ms: 1.18x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 93.2 ms: 1.19x slower                                                  |
| sympy_expand               | 457 ms                                                       | 542 ms: 1.19x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 23.7 ms: 1.20x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.87 ms: 1.20x slower                                                  |
| sympy_str                  | 275 ms                                                       | 330 ms: 1.20x slower                                                   |
| django_template            | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.7 ms: 1.20x slower                                                  |
| richards                   | 45.2 ms                                                      | 55.3 ms: 1.22x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 360 us: 1.22x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.5 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.54 ms: 1.23x slower                                                  |
| richards_super             | 51.6 ms                                                      | 63.9 ms: 1.24x slower                                                  |
| raytrace                   | 253 ms                                                       | 316 ms: 1.25x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.26x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 86.4 ms: 1.27x slower                                                  |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                   |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.3 ms: 1.35x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.55 ms: 1.46x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.46x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 91.7 ms: 8.34x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250131-3.14.0a4+-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.061x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.34x