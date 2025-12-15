# Results vs. 3.13.0rc2

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 241 ms: 1.08x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 56.7 ms: 1.18x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 523 ms: 1.68x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 282 ms: 1.64x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| async_tree_none            | 354 ms                                                       | 231 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 456 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 459 ms: 1.39x faster                                                   |
| async_generators           | 377 ms                                                       | 319 ms: 1.18x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 437 ms: 1.16x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.44 sec: 1.05x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 66.3 ms: 1.17x faster                                                  |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                   |
| nbody          | 85.1 ms                                                      | 80.5 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 117 ms: 1.13x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 181 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.07 ms: 1.16x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 29.5 us: 1.10x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 53.9 ms: 1.10x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 78.3 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 199 us: 1.06x faster                                                   |
| json_loads           | 27.0 us                                                      | 25.9 us: 1.04x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.77 us: 1.03x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 291 us: 1.01x faster                                                   |
| unpickle_list        | 4.71 us                                                      | 4.66 us: 1.01x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.04 sec: 1.02x slower                                                 |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| pickle               | 11.3 us                                                      | 12.4 us: 1.09x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 149 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.1 ms: 1.13x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 45.5 ms: 1.07x faster                                                  |
| django_template | 34.1 ms                                                      | 32.4 ms: 1.05x faster                                                  |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.09 sec: 2.16x faster                                                 |
| async_tree_io              | 876 ms                                                       | 523 ms: 1.68x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 282 ms: 1.64x faster                                                   |
| deepcopy                   | 355 us                                                       | 218 us: 1.63x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 24.2 us: 1.61x faster                                                  |
| async_tree_none            | 354 ms                                                       | 231 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 456 ms: 1.46x faster                                                   |
| go                         | 141 ms                                                       | 97.2 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 459 ms: 1.39x faster                                                   |
| scimark_sor                | 134 ms                                                       | 97.1 ms: 1.38x faster                                                  |
| spectral_norm              | 111 ms                                                       | 83.2 ms: 1.33x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.35 us: 1.33x faster                                                  |
| scimark_fft                | 349 ms                                                       | 266 ms: 1.31x faster                                                   |
| richards                   | 45.2 ms                                                      | 36.9 ms: 1.23x faster                                                  |
| logging_silent             | 103 ns                                                       | 84.6 ns: 1.21x faster                                                  |
| richards_super             | 51.6 ms                                                      | 42.6 ms: 1.21x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.0 ms: 1.19x faster                                                  |
| async_generators           | 377 ms                                                       | 319 ms: 1.18x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 56.7 ms: 1.18x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.00 ms: 1.18x faster                                                  |
| float                      | 77.5 ms                                                      | 66.3 ms: 1.17x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.07 ms: 1.16x faster                                                  |
| pyflate                    | 449 ms                                                       | 388 ms: 1.16x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 437 ms: 1.16x faster                                                   |
| pylint                     | 317 ms                                                       | 274 ms: 1.16x faster                                                   |
| chaos                      | 57.3 ms                                                      | 50.0 ms: 1.14x faster                                                  |
| regex_compile              | 132 ms                                                       | 117 ms: 1.13x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 66.2 ms: 1.13x faster                                                  |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.13x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 19.1 ms: 1.13x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.0 ms: 1.13x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 100 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 17.8 ms: 1.11x faster                                                  |
| coverage                   | 83.0 ms                                                      | 74.7 ms: 1.11x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 29.5 us: 1.10x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 53.9 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.46 ms: 1.10x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.62 us: 1.10x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 141 us: 1.09x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.37 sec: 1.09x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 675 ms: 1.09x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 78.3 ms: 1.09x faster                                                  |
| thrift                     | 778 us                                                       | 714 us: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.88 ms: 1.08x faster                                                  |
| 2to3                       | 260 ms                                                       | 241 ms: 1.08x faster                                                   |
| raytrace                   | 253 ms                                                       | 236 ms: 1.07x faster                                                   |
| genshi_xml                 | 48.8 ms                                                      | 45.5 ms: 1.07x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 73.8 ms: 1.06x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.44 us: 1.06x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 147 ms: 1.06x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.2 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 199 us: 1.06x faster                                                   |
| nbody                      | 85.1 ms                                                      | 80.5 ms: 1.06x faster                                                  |
| django_template            | 34.1 ms                                                      | 32.4 ms: 1.05x faster                                                  |
| sympy_str                  | 275 ms                                                       | 261 ms: 1.05x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.06 sec: 1.05x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.44 sec: 1.05x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                  |
| sympy_expand               | 457 ms                                                       | 442 ms: 1.03x faster                                                   |
| pickle_list                | 4.93 us                                                      | 4.77 us: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.2 ms: 1.03x faster                                                  |
| pickle_pure_python         | 294 us                                                       | 291 us: 1.01x faster                                                   |
| unpickle_list              | 4.71 us                                                      | 4.66 us: 1.01x faster                                                  |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                   |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.01x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.04 sec: 1.02x slower                                                 |
| unpickle                   | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| unpack_sequence            | 44.8 ns                                                      | 48.2 ns: 1.08x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.4 us: 1.09x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 149 ms: 1.09x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.30 ms: 1.37x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.26 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 2.00 ms: 1.49x slower                                                  |
| telco                      | 7.82 ms                                                      | 153 ms: 19.52x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 372 ms: 33.80x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-CLANG/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.18x