# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.091x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                 |
| html5lib       | 67.0 ms                                                      | 64.3 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 585 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 449 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 356 ms: 1.06x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 56.7 ms: 1.37x faster                                                  |
| nbody          | 85.1 ms                                                      | 72.9 ms: 1.17x faster                                                  |
| pidigits       | 217 ms                                                       | 205 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.19x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                                  |
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| regex_dna      | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.66 sec: 1.21x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 177 us: 1.18x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.1 ms: 1.14x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 77.7 ms: 1.10x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 281 us: 1.05x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 31.7 us: 1.03x faster                                                  |
| pickle_list          | 4.93 us                                                      | 5.07 us: 1.03x slower                                                  |
| unpickle             | 14.3 us                                                      | 14.7 us: 1.03x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.05x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.15 us: 1.09x slower                                                  |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                                  |
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                  |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 52.2 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.7 ms: 2.55x faster                                                  |
| richards_super             | 51.6 ms                                                      | 21.6 ms: 2.39x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.75x faster                                                 |
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                   |
| deepcopy                   | 355 us                                                       | 223 us: 1.59x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 24.6 us: 1.59x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 585 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| go                         | 141 ms                                                       | 91.9 ms: 1.53x faster                                                  |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| float                      | 77.5 ms                                                      | 56.7 ms: 1.37x faster                                                  |
| scimark_sor                | 134 ms                                                       | 99.9 ms: 1.35x faster                                                  |
| scimark_fft                | 349 ms                                                       | 262 ms: 1.33x faster                                                   |
| spectral_norm              | 111 ms                                                       | 84.0 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.43 us: 1.28x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.2 ms: 1.25x faster                                                  |
| pyflate                    | 449 ms                                                       | 362 ms: 1.24x faster                                                   |
| logging_silent             | 103 ns                                                       | 83.7 ns: 1.22x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.66 sec: 1.21x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 177 us: 1.18x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 630 ms: 1.17x faster                                                   |
| nbody                      | 85.1 ms                                                      | 72.9 ms: 1.17x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.69 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.31 sec: 1.14x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.1 ms: 1.14x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 449 ms: 1.12x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 100 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.01 sec: 1.11x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.26 ms: 1.11x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 77.7 ms: 1.10x faster                                                  |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                                  |
| chaos                      | 57.3 ms                                                      | 53.2 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| regex_dna                  | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| async_generators           | 377 ms                                                       | 356 ms: 1.06x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 70.6 ms: 1.06x faster                                                  |
| pidigits                   | 217 ms                                                       | 205 ms: 1.06x faster                                                   |
| fannkuch                   | 370 ms                                                       | 350 ms: 1.06x faster                                                   |
| pickle_pure_python         | 294 us                                                       | 281 us: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 64.3 ms: 1.04x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.91 us: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 749 us: 1.04x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.47 sec: 1.03x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.1 ms: 1.03x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.9 ms: 1.03x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 31.7 us: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.67 us: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.03 ms: 1.01x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 80.4 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| pickle_list                | 4.93 us                                                      | 5.07 us: 1.03x slower                                                  |
| unpickle                   | 14.3 us                                                      | 14.7 us: 1.03x slower                                                  |
| generators                 | 28.8 ms                                                      | 30.0 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| raytrace                   | 253 ms                                                       | 264 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.05x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 52.2 ms: 1.07x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 168 ms: 1.08x slower                                                   |
| unpickle_list              | 4.71 us                                                      | 5.15 us: 1.09x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| sympy_expand               | 457 ms                                                       | 507 ms: 1.11x slower                                                   |
| sympy_str                  | 275 ms                                                       | 307 ms: 1.12x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.24 ms: 1.35x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 69.0 ns: 1.54x slower                                                  |
| telco                      | 7.82 ms                                                      | 162 ms: 20.75x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 239 ms: 21.70x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x