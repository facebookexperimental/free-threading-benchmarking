# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 244 ms: 1.06x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 56.6 ms: 1.18x faster                                                  |
| Geometric mean | (ref)                                                        | 1.10x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 519 ms: 1.69x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 279 ms: 1.66x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 557 ms: 1.64x faster                                                   |
| async_tree_none            | 354 ms                                                       | 229 ms: 1.54x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 230 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 457 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 289 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 456 ms: 1.40x faster                                                   |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 449 ms: 1.12x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 65.4 ms: 1.19x faster                                                  |
| pidigits       | 217 ms                                                       | 198 ms: 1.10x faster                                                   |
| nbody          | 85.1 ms                                                      | 81.1 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 117 ms: 1.13x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.04 ms: 1.16x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.74 sec: 1.15x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 54.5 ms: 1.09x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 79.0 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.42 us: 1.07x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 201 us: 1.04x faster                                                   |
| json_loads           | 27.0 us                                                      | 26.0 us: 1.04x faster                                                  |
| pickle_list          | 4.93 us                                                      | 5.03 us: 1.02x slower                                                  |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 148 ms: 1.09x slower                                                   |
| pickle               | 11.3 us                                                      | 12.9 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): pickle_pure_python, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.3 ms: 1.12x faster                                                  |
| django_template | 34.1 ms                                                      | 31.7 ms: 1.08x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 45.9 ms: 1.06x faster                                                  |
| mako            | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.09 sec: 2.16x faster                                                 |
| deepcopy                   | 355 us                                                       | 210 us: 1.69x faster                                                   |
| async_tree_io              | 876 ms                                                       | 519 ms: 1.69x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 279 ms: 1.66x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 557 ms: 1.64x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 24.6 us: 1.59x faster                                                  |
| async_tree_none            | 354 ms                                                       | 229 ms: 1.54x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 230 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 457 ms: 1.46x faster                                                   |
| go                         | 141 ms                                                       | 97.2 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 289 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 456 ms: 1.40x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.27 us: 1.37x faster                                                  |
| scimark_fft                | 349 ms                                                       | 255 ms: 1.37x faster                                                   |
| scimark_sor                | 134 ms                                                       | 98.4 ms: 1.37x faster                                                  |
| spectral_norm              | 111 ms                                                       | 81.6 ms: 1.36x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.64 ms: 1.30x faster                                                  |
| logging_silent             | 103 ns                                                       | 81.2 ns: 1.26x faster                                                  |
| richards                   | 45.2 ms                                                      | 36.4 ms: 1.24x faster                                                  |
| richards_super             | 51.6 ms                                                      | 41.7 ms: 1.24x faster                                                  |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.9 ms: 1.19x faster                                                  |
| float                      | 77.5 ms                                                      | 65.4 ms: 1.19x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 56.6 ms: 1.18x faster                                                  |
| pyflate                    | 449 ms                                                       | 383 ms: 1.17x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.04 ms: 1.16x faster                                                  |
| pylint                     | 317 ms                                                       | 276 ms: 1.15x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.74 sec: 1.15x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 16.8 ms: 1.14x faster                                                  |
| chaos                      | 57.3 ms                                                      | 50.2 ms: 1.14x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 99.1 ms: 1.14x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.1 ms: 1.13x faster                                                  |
| regex_compile              | 132 ms                                                       | 117 ms: 1.13x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 449 ms: 1.12x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 19.3 ms: 1.12x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.36 ms: 1.12x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.80 ms: 1.12x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.52 us: 1.12x faster                                                  |
| comprehensions             | 16.5 us                                                      | 14.8 us: 1.11x faster                                                  |
| coverage                   | 83.0 ms                                                      | 74.7 ms: 1.11x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 668 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.36 sec: 1.10x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.24 us: 1.10x faster                                                  |
| pidigits                   | 217 ms                                                       | 198 ms: 1.10x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.2 ms: 1.09x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 54.5 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 143 us: 1.08x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 79.0 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| raytrace                   | 253 ms                                                       | 234 ms: 1.08x faster                                                   |
| django_template            | 34.1 ms                                                      | 31.7 ms: 1.08x faster                                                  |
| unpickle_list              | 4.71 us                                                      | 4.42 us: 1.07x faster                                                  |
| 2to3                       | 260 ms                                                       | 244 ms: 1.06x faster                                                   |
| thrift                     | 778 us                                                       | 733 us: 1.06x faster                                                   |
| genshi_xml                 | 48.8 ms                                                      | 45.9 ms: 1.06x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.2 ms: 1.06x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 147 ms: 1.06x faster                                                   |
| nbody                      | 85.1 ms                                                      | 81.1 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 201 us: 1.04x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 75.3 ms: 1.04x faster                                                  |
| sympy_str                  | 275 ms                                                       | 263 ms: 1.04x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| json_loads                 | 27.0 us                                                      | 26.0 us: 1.04x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                                  |
| sympy_expand               | 457 ms                                                       | 446 ms: 1.02x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                  |
| mako                       | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| pickle_list                | 4.93 us                                                      | 5.03 us: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| unpickle                   | 14.3 us                                                      | 15.0 us: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 148 ms: 1.09x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.9 us: 1.13x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 52.4 ns: 1.17x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.26 ms: 1.38x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.37 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 2.05 ms: 1.53x slower                                                  |
| telco                      | 7.82 ms                                                      | 153 ms: 19.55x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 317 ms: 28.83x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (4): pickle_pure_python, meteor_contest, json, pickle_dict
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d-CLANG/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.18x