# Results vs. 3.13.0rc2

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 244 ms: 1.06x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.2 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 543 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 581 ms: 1.57x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| async_tree_none            | 354 ms                                                       | 239 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 521 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 215 ms: 1.01x faster                                                   |
| nbody          | 85.1 ms                                                      | 90.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.84 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.28 us: 1.07x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.20 us: 1.10x slower                                                  |
| pickle               | 11.3 us                                                      | 12.7 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                  |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.06x faster                                                 |
| async_tree_io              | 876 ms                                                       | 543 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 581 ms: 1.57x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                                  |
| async_tree_none            | 354 ms                                                       | 239 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| go                         | 141 ms                                                       | 106 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 521 ms: 1.28x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.9 ms: 1.18x faster                                                  |
| scimark_fft                | 349 ms                                                       | 300 ms: 1.16x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.2 ms: 1.13x faster                                                  |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                   |
| float                      | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.1 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                   |
| pyflate                    | 449 ms                                                       | 413 ms: 1.09x faster                                                   |
| regex_compile              | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.35 ms: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                  |
| unpack_sequence            | 44.8 ns                                                      | 41.5 ns: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.8 ms: 1.08x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.55 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 685 ms: 1.08x faster                                                   |
| richards                   | 45.2 ms                                                      | 42.1 ms: 1.07x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.84 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                 |
| 2to3                       | 260 ms                                                       | 244 ms: 1.06x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.06x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.0 ms: 1.04x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.8 us: 1.04x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.1 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.9 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.66 us: 1.03x faster                                                  |
| thrift                     | 778 us                                                       | 758 us: 1.03x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                   |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| pidigits                   | 217 ms                                                       | 215 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                   |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.7 ms: 1.01x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 470 ms: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.33 us: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.0 ms: 1.06x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.28 us: 1.07x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 5.20 us: 1.10x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.7 us: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.43 ms: 1.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 329 ms: 29.93x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (3): unpickle, pickle_dict, nqueens
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x