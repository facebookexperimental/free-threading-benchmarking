# Results vs. 3.13.0rc2

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.035x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 550 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 478 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 453 ms: 1.12x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                  |
| regex_dna      | 180 ms                                                       | 188 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.87 sec: 1.08x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                   |
| pickle_list          | 4.93 us                                                      | 5.12 us: 1.04x slower                                                  |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| pickle               | 11.3 us                                                      | 12.5 us: 1.11x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.30 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.6 ms: 1.00x faster                                                  |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                  |
| mako            | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.03x faster                                                 |
| async_tree_io              | 876 ms                                                       | 550 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| deepcopy                   | 355 us                                                       | 232 us: 1.53x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 478 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| go                         | 141 ms                                                       | 106 ms: 1.32x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.52 us: 1.24x faster                                                  |
| spectral_norm              | 111 ms                                                       | 92.5 ms: 1.20x faster                                                  |
| scimark_fft                | 349 ms                                                       | 306 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                  |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.2 ms: 1.12x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 453 ms: 1.12x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.3 ms: 1.11x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                   |
| richards                   | 45.2 ms                                                      | 41.5 ms: 1.09x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.5 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.87 sec: 1.08x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 709 ms: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.95 us: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.56 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.6 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.74 us: 1.01x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.3 us: 1.01x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.6 ms: 1.00x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.00x faster                                                 |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 277 ms: 1.01x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.5 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.12 us: 1.04x slower                                                  |
| unpickle                   | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 46.7 ns: 1.04x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.33 us: 1.05x slower                                                  |
| fannkuch                   | 370 ms                                                       | 390 ms: 1.05x slower                                                   |
| json                       | 4.93 ms                                                      | 5.20 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 483 ms: 1.06x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.5 us: 1.11x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 5.30 us: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.35 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.40x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 328 ms: 29.85x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): thrift, sympy_sum, raytrace
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x