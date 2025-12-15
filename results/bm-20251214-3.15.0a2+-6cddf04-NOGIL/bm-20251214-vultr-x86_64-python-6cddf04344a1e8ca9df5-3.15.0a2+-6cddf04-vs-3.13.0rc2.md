# Results vs. 3.13.0rc2

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.067x slower
- HPT reliability: 93.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 279 ms: 1.08x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 324 ms: 1.28x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 526 ms: 1.21x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 459 ms: 1.10x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.75 sec: 1.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| float          | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| nbody          | 85.1 ms                                                      | 123 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                  |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 32.1 us: 1.01x faster                                                  |
| pickle_list          | 4.93 us                                                      | 5.14 us: 1.04x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 335 us: 1.14x slower                                                   |
| unpickle             | 14.3 us                                                      | 16.3 us: 1.14x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.30 sec: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 70.3 ms: 1.19x slower                                                  |
| json_loads           | 27.0 us                                                      | 32.2 us: 1.19x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.64 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.68 ms: 1.31x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.1 ms: 1.19x slower                                                  |
| django_template | 34.1 ms                                                      | 41.1 ms: 1.20x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                  |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.91 ms: 1.65x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.16 ms: 1.54x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.5 us: 1.28x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 324 ms: 1.28x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.28x faster                                                   |
| deepcopy                   | 355 us                                                       | 279 us: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 526 ms: 1.21x faster                                                   |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                   |
| pidigits                   | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 459 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.08 us: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.2 ms: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.98 us: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                  |
| scimark_fft                | 349 ms                                                       | 341 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.36 sec: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                   |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                   |
| pickle_dict                | 32.5 us                                                      | 32.1 us: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.00x slower                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                       | 458 ms: 1.02x slower                                                   |
| pickle_list                | 4.93 us                                                      | 5.14 us: 1.04x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 788 ms: 1.07x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.40 ms: 1.07x slower                                                  |
| generators                 | 28.8 ms                                                      | 30.9 ms: 1.07x slower                                                  |
| 2to3                       | 260 ms                                                       | 279 ms: 1.08x slower                                                   |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 21.6 ms: 1.09x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.9 us: 1.09x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.64 sec: 1.09x slower                                                 |
| chaos                      | 57.3 ms                                                      | 62.9 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.47 ms: 1.10x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| json                       | 4.93 ms                                                      | 5.48 ms: 1.11x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.87 us: 1.12x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.12x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.28 ms: 1.12x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 176 ms: 1.13x slower                                                   |
| thrift                     | 778 us                                                       | 882 us: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 89.3 ms: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                   |
| unpickle                   | 14.3 us                                                      | 16.3 us: 1.14x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.7 ms: 1.14x slower                                                  |
| sympy_expand               | 457 ms                                                       | 522 ms: 1.14x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.30 sec: 1.14x slower                                                 |
| sympy_str                  | 275 ms                                                       | 315 ms: 1.15x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.86 us: 1.15x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.5 ms: 1.15x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.75 sec: 1.16x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.16x slower                                                   |
| raytrace                   | 253 ms                                                       | 296 ms: 1.17x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 70.3 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.6 ms: 1.19x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.1 ms: 1.19x slower                                                  |
| json_loads                 | 27.0 us                                                      | 32.2 us: 1.19x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 5.64 us: 1.20x slower                                                  |
| meteor_contest             | 102 ms                                                       | 122 ms: 1.20x slower                                                   |
| django_template            | 34.1 ms                                                      | 41.1 ms: 1.20x slower                                                  |
| fannkuch                   | 370 ms                                                       | 455 ms: 1.23x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.90 ms: 1.25x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 85.8 ms: 1.26x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 57.0 ns: 1.27x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.68 ms: 1.31x slower                                                  |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                  |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.44x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                  |
| telco                      | 7.82 ms                                                      | 176 ms: 22.55x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): pylint, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-NOGIL/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x slower

# HPT report

- Reliability score: 93.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x