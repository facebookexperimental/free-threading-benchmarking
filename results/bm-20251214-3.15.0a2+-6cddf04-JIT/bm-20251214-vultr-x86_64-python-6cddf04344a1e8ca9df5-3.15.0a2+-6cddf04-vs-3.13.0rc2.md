# Results vs. 3.13.0rc2

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.091x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 590 ms: 1.55x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 480 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.31x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 442 ms: 1.14x faster                                                   |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 58.9 ms: 1.31x faster                                                  |
| nbody          | 85.1 ms                                                      | 71.5 ms: 1.19x faster                                                  |
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                   |
| Geometric mean | (ref)                                                        | 1.20x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| regex_compile  | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| regex_dna      | 180 ms                                                       | 167 ms: 1.08x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 182 us: 1.16x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.9 ms: 1.13x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.41 ms: 1.12x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 77.3 ms: 1.10x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 288 us: 1.02x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.98 sec: 1.02x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.06 us: 1.03x slower                                                  |
| pickle               | 11.3 us                                                      | 12.4 us: 1.09x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.14 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                  |
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 53.0 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 19.7 ms: 2.30x faster                                                  |
| richards_super             | 51.6 ms                                                      | 23.8 ms: 2.17x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 24.3 us: 1.61x faster                                                  |
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 590 ms: 1.55x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                   |
| go                         | 141 ms                                                       | 100 ms: 1.41x faster                                                   |
| scimark_fft                | 349 ms                                                       | 249 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 480 ms: 1.39x faster                                                   |
| scimark_sor                | 134 ms                                                       | 97.7 ms: 1.38x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.31x faster                                                   |
| float                      | 77.5 ms                                                      | 58.9 ms: 1.31x faster                                                  |
| spectral_norm              | 111 ms                                                       | 85.3 ms: 1.30x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.50 us: 1.25x faster                                                  |
| pyflate                    | 449 ms                                                       | 371 ms: 1.21x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.6 ms: 1.20x faster                                                  |
| logging_silent             | 103 ns                                                       | 86.1 ns: 1.19x faster                                                  |
| nbody                      | 85.1 ms                                                      | 71.5 ms: 1.19x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 182 us: 1.16x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 639 ms: 1.15x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.73 ms: 1.15x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 442 ms: 1.14x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.9 ms: 1.13x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.33 sec: 1.13x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.41 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.25 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.01 sec: 1.11x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 77.3 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.10x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 103 ms: 1.09x faster                                                   |
| regex_compile              | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| regex_dna                  | 180 ms                                                       | 167 ms: 1.08x faster                                                   |
| chaos                      | 57.3 ms                                                      | 53.2 ms: 1.08x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                  |
| thrift                     | 778 us                                                       | 735 us: 1.06x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.82 us: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| meteor_contest             | 102 ms                                                       | 97.9 ms: 1.04x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| pickle_dict                | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.1 ms: 1.03x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 73.0 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.2 ms: 1.02x faster                                                  |
| pickle_pure_python         | 294 us                                                       | 288 us: 1.02x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.70 us: 1.02x faster                                                  |
| fannkuch                   | 370 ms                                                       | 363 ms: 1.02x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.98 sec: 1.02x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.2 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.08 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.06 us: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 53.0 ms: 1.09x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.4 us: 1.09x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 5.14 us: 1.09x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 85.9 ms: 1.09x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.48 ms: 1.43x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 81.2 ns: 1.81x slower                                                  |
| telco                      | 7.82 ms                                                      | 162 ms: 20.69x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 238 ms: 21.67x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (6): pylint, json, sqlite_synth, html5lib, typing_runtime_protocols, unpickle
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, docutils, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x