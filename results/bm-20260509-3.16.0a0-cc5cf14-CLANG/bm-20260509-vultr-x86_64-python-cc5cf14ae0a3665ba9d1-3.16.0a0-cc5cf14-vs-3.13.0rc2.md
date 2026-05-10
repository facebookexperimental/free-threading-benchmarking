# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.34 sec: 1.12x faster                                                |
| html5lib       | 67.0 ms                                                      | 58.6 ms: 1.14x faster                                                 |
| Geometric mean | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 524 ms: 1.27x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 367 ms: 1.26x faster                                                  |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                  |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 359 ms: 1.15x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 294 ms: 1.14x faster                                                  |
| async_generators           | 377 ms                                                       | 335 ms: 1.13x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.48 sec: 1.02x faster                                                |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 73.9 ms: 1.05x faster                                                 |
| nbody          | 85.1 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 122 ms: 1.09x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| regex_dna      | 180 ms                                                       | 193 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.36 ms: 1.12x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 31.9 us: 1.02x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.6 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.7 ms: 1.01x faster                                                 |
| pickle_list          | 4.93 us                                                      | 4.88 us: 1.01x faster                                                 |
| unpickle_list        | 4.71 us                                                      | 4.67 us: 1.01x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                  |
| unpickle             | 14.3 us                                                      | 15.5 us: 1.08x slower                                                 |
| pickle               | 11.3 us                                                      | 13.2 us: 1.17x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 160 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 33.3 ms: 1.02x faster                                                 |
| mako            | 11.3 ms                                                      | 12.9 ms: 1.14x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.10 sec: 2.14x faster                                                |
| deepcopy                   | 355 us                                                       | 222 us: 1.60x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.2 us: 1.49x faster                                                 |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                  |
| spectral_norm              | 111 ms                                                       | 86.0 ms: 1.29x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.42 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 524 ms: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 367 ms: 1.26x faster                                                  |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                  |
| logging_silent             | 103 ns                                                       | 83.0 ns: 1.24x faster                                                 |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                  |
| scimark_fft                | 349 ms                                                       | 291 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 359 ms: 1.15x faster                                                  |
| richards_super             | 51.6 ms                                                      | 44.8 ms: 1.15x faster                                                 |
| richards                   | 45.2 ms                                                      | 39.3 ms: 1.15x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 294 ms: 1.14x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 58.6 ms: 1.14x faster                                                 |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 335 ms: 1.13x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.36 ms: 1.12x faster                                                 |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.34 sec: 1.12x faster                                                |
| comprehensions             | 16.5 us                                                      | 14.7 us: 1.12x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.54 us: 1.11x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                 |
| pyflate                    | 449 ms                                                       | 407 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 59.4 ms: 1.10x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.28 ms: 1.10x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.23 us: 1.10x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 68.1 ms: 1.10x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                |
| chaos                      | 57.3 ms                                                      | 52.3 ms: 1.10x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 72.3 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 122 ms: 1.09x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 18.3 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.13 sec: 1.08x faster                                                |
| typing_runtime_protocols   | 155 us                                                       | 146 us: 1.06x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                  |
| float                      | 77.5 ms                                                      | 73.9 ms: 1.05x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 149 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.74 ms: 1.04x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.6 ms: 1.04x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.00 ms: 1.04x faster                                                 |
| sympy_str                  | 275 ms                                                       | 264 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 754 us: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| raytrace                   | 253 ms                                                       | 245 ms: 1.03x faster                                                  |
| sympy_expand               | 457 ms                                                       | 444 ms: 1.03x faster                                                  |
| django_template            | 34.1 ms                                                      | 33.3 ms: 1.02x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.48 sec: 1.02x faster                                                |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| pickle_dict                | 32.5 us                                                      | 31.9 us: 1.02x faster                                                 |
| nbody                      | 85.1 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.6 us: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.01x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.7 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 729 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                 |
| pickle_list                | 4.93 us                                                      | 4.88 us: 1.01x faster                                                 |
| unpickle_list              | 4.71 us                                                      | 4.67 us: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 70.9 ms: 1.04x slower                                                 |
| meteor_contest             | 102 ms                                                       | 107 ms: 1.06x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                  |
| regex_dna                  | 180 ms                                                       | 193 ms: 1.07x slower                                                  |
| unpickle                   | 14.3 us                                                      | 15.5 us: 1.08x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.9 ms: 1.14x slower                                                 |
| pickle                     | 11.3 us                                                      | 13.2 us: 1.17x slower                                                 |
| unpack_sequence            | 44.8 ns                                                      | 52.5 ns: 1.17x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 160 ms: 1.17x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.97 ms: 1.26x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.29 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.95 ms: 1.45x slower                                                 |
| telco                      | 7.82 ms                                                      | 157 ms: 20.01x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 313 ms: 28.48x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): generators
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x