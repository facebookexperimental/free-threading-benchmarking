# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.5 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 478 ms: 1.50x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 453 ms: 1.15x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 91.8 ms: 1.03x slower                                                  |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.87 sec: 1.13x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.1 ms: 1.03x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.02x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                                  |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.12 us: 1.07x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.30 us: 1.13x slower                                                  |
| pickle               | 10.9 us                                                | 12.5 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                  |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 232 us: 1.52x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 478 ms: 1.50x faster                                                   |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.2 ms: 1.25x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.23x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.52 us: 1.22x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.5 ms: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.3 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 453 ms: 1.15x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                  |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.6 ms: 1.13x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.87 sec: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                 |
| scimark_fft                | 342 ms                                                 | 306 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.95 us: 1.11x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 46.7 ns: 1.11x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 69.1 ms: 1.11x faster                                                  |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.5 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                                   |
| logging_format             | 7.35 us                                                | 6.74 us: 1.09x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.69 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| html5lib                   | 63.6 ms                                                | 60.5 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 709 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.1 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.02x faster                                                   |
| thrift                     | 791 us                                                 | 775 us: 1.02x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| nqueens                    | 80.1 ms                                                | 79.5 ms: 1.01x faster                                                  |
| pickle_dict                | 31.8 us                                                | 31.6 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                  |
| django_template            | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                  |
| nbody                      | 89.3 ms                                                | 91.8 ms: 1.03x slower                                                  |
| sympy_expand               | 468 ms                                                 | 483 ms: 1.03x slower                                                   |
| json                       | 5.02 ms                                                | 5.20 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.56 ms: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 390 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.33 us: 1.06x slower                                                  |
| unpickle                   | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.12 us: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| unpickle_list              | 4.67 us                                                | 5.30 us: 1.13x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                  |
| pickle                     | 10.9 us                                                | 12.5 us: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.35 ms: 1.26x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.73x slower                                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.46x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 328 ms: 30.40x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): coroutines, pickle_pure_python
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x