# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.061x slower
- HPT reliability: 90.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.06x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 518 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 461 ms: 1.10x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.75 sec: 1.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.18x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 199 ms: 1.09x faster                                                   |
| float          | 77.5 ms                                                      | 73.7 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 124 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| regex_compile  | 132 ms                                                       | 140 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| pickle_list          | 4.93 us                                                      | 4.90 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                  |
| pickle               | 11.3 us                                                      | 11.9 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 237 us: 1.13x slower                                                   |
| unpickle             | 14.3 us                                                      | 16.3 us: 1.14x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 337 us: 1.14x slower                                                   |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.47 us: 1.16x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.66 ms: 1.31x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.0 ms: 1.19x slower                                                  |
| django_template | 34.1 ms                                                      | 41.2 ms: 1.21x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 27.2 ms: 1.26x slower                                                  |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.79x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.66x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.05 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                   |
| deepcopy                   | 355 us                                                       | 269 us: 1.32x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.5 us: 1.28x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 518 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                   |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.11x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 461 ms: 1.10x faster                                                   |
| pidigits                   | 217 ms                                                       | 199 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.08 us: 1.06x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.95 us: 1.06x faster                                                  |
| float                      | 77.5 ms                                                      | 73.7 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 72.0 ms: 1.04x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                 |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| pickle_list                | 4.93 us                                                      | 4.90 us: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.00x slower                                                   |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                 |
| pyflate                    | 449 ms                                                       | 463 ms: 1.03x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 766 ms: 1.04x slower                                                   |
| pickle                     | 11.3 us                                                      | 11.9 us: 1.05x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.06x slower                                                 |
| regex_compile              | 132 ms                                                       | 140 ms: 1.06x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.59 sec: 1.06x slower                                                 |
| 2to3                       | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.43 ms: 1.07x slower                                                  |
| json                       | 4.93 ms                                                      | 5.29 ms: 1.07x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.7 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.1 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.50 ms: 1.12x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.4 ms: 1.12x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 175 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.93 us: 1.13x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 237 us: 1.13x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 88.7 ms: 1.13x slower                                                  |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                   |
| richards                   | 45.2 ms                                                      | 51.1 ms: 1.13x slower                                                  |
| richards_super             | 51.6 ms                                                      | 58.5 ms: 1.13x slower                                                  |
| sympy_expand               | 457 ms                                                       | 518 ms: 1.13x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.78 us: 1.14x slower                                                  |
| unpickle                   | 14.3 us                                                      | 16.3 us: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 337 us: 1.14x slower                                                   |
| thrift                     | 778 us                                                       | 893 us: 1.15x slower                                                   |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.16x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.61 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.75 sec: 1.16x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.47 us: 1.16x slower                                                  |
| raytrace                   | 253 ms                                                       | 294 ms: 1.16x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.50 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.0 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.7 ms: 1.19x slower                                                  |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                                   |
| django_template            | 34.1 ms                                                      | 41.2 ms: 1.21x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 55.2 ns: 1.23x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.24x slower                                                   |
| fannkuch                   | 370 ms                                                       | 463 ms: 1.25x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 27.2 ms: 1.26x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.8 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.66 ms: 1.31x slower                                                  |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 85.1 ms                                                      | 124 ms: 1.46x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                  |
| telco                      | 7.82 ms                                                      | 176 ms: 22.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (2): pylint, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d-NOGIL/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.061x slower

# HPT report

- Reliability score: 90.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x