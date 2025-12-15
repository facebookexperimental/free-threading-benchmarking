# Results vs. 3.12.6

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 241 ms: 1.09x faster                                                   |
| docutils       | 2.64 sec                                               | 2.47 sec: 1.07x faster                                                 |
| html5lib       | 63.6 ms                                                | 56.7 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 523 ms: 2.07x faster                                                   |
| async_tree_none            | 464 ms                                                 | 231 ms: 2.01x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 282 ms: 1.97x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 565 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 459 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 456 ms: 1.57x faster                                                   |
| async_generators           | 384 ms                                                 | 319 ms: 1.21x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 437 ms: 1.19x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.44 sec: 1.04x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| nbody          | 89.3 ms                                                | 80.5 ms: 1.11x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 117 ms: 1.22x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.4 ms                                                | 9.07 ms: 1.14x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 199 us: 1.11x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 53.9 ms: 1.09x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 78.3 ms: 1.09x faster                                                  |
| pickle_dict          | 31.8 us                                                | 29.5 us: 1.08x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 291 us: 1.06x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.04 sec: 1.03x faster                                                 |
| json_loads           | 26.5 us                                                | 25.9 us: 1.02x faster                                                  |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| xml_etree_parse      | 139 ms                                                 | 149 ms: 1.07x slower                                                   |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.1 ms: 1.19x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 45.5 ms: 1.10x faster                                                  |
| django_template | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.09 sec: 2.22x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 523 ms: 2.07x faster                                                   |
| async_tree_none            | 464 ms                                                 | 231 ms: 2.01x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 282 ms: 1.97x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 565 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.89x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 24.2 us: 1.67x faster                                                  |
| deepcopy                   | 352 us                                                 | 218 us: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 459 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 456 ms: 1.57x faster                                                   |
| go                         | 139 ms                                                 | 97.2 ms: 1.43x faster                                                  |
| comprehensions             | 19.8 us                                                | 14.6 us: 1.36x faster                                                  |
| scimark_sor                | 130 ms                                                 | 97.1 ms: 1.34x faster                                                  |
| spectral_norm              | 110 ms                                                 | 83.2 ms: 1.32x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.35 us: 1.31x faster                                                  |
| logging_silent             | 109 ns                                                 | 84.6 ns: 1.29x faster                                                  |
| scimark_fft                | 342 ms                                                 | 266 ms: 1.28x faster                                                   |
| raytrace                   | 299 ms                                                 | 236 ms: 1.27x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.0 ms: 1.26x faster                                                  |
| chaos                      | 62.8 ms                                                | 50.0 ms: 1.26x faster                                                  |
| richards                   | 45.9 ms                                                | 36.9 ms: 1.24x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 55.0 ms: 1.24x faster                                                  |
| regex_compile              | 142 ms                                                 | 117 ms: 1.22x faster                                                   |
| float                      | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| richards_super             | 51.9 ms                                                | 42.6 ms: 1.22x faster                                                  |
| async_generators           | 384 ms                                                 | 319 ms: 1.21x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.88 ms: 1.20x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.1 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.2 ms: 1.19x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 437 ms: 1.19x faster                                                   |
| generators                 | 32.2 ms                                                | 27.2 ms: 1.18x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.62 us: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                 |
| pylint                     | 319 ms                                                 | 274 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.2 ms: 1.16x faster                                                  |
| pyflate                    | 448 ms                                                 | 388 ms: 1.16x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 141 us: 1.16x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.07 ms: 1.14x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 100 ms: 1.14x faster                                                   |
| logging_format             | 7.35 us                                                | 6.44 us: 1.14x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 147 ms: 1.13x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.46 ms: 1.13x faster                                                  |
| html5lib                   | 63.6 ms                                                | 56.7 ms: 1.12x faster                                                  |
| sympy_str                  | 292 ms                                                 | 261 ms: 1.12x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 199 us: 1.11x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                 |
| nbody                      | 89.3 ms                                                | 80.5 ms: 1.11x faster                                                  |
| thrift                     | 791 us                                                 | 714 us: 1.11x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 45.5 ms: 1.10x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 675 ms: 1.10x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.06 sec: 1.10x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.00 ms: 1.10x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 53.9 ms: 1.09x faster                                                  |
| 2to3                       | 264 ms                                                 | 241 ms: 1.09x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 78.3 ms: 1.09x faster                                                  |
| nqueens                    | 80.1 ms                                                | 73.8 ms: 1.08x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 48.2 ns: 1.08x faster                                                  |
| pickle_dict                | 31.8 us                                                | 29.5 us: 1.08x faster                                                  |
| django_template            | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.47 sec: 1.07x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| sympy_expand               | 468 ms                                                 | 442 ms: 1.06x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 291 us: 1.06x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.44 sec: 1.04x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.04 sec: 1.03x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.9 us: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                   |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                   |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| coverage                   | 71.4 ms                                                | 74.7 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| unpickle                   | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 149 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| pickle                     | 10.9 us                                                | 12.4 us: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.30 ms: 1.24x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.26 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 2.00 ms: 1.83x slower                                                  |
| telco                      | 6.53 ms                                                | 153 ms: 23.39x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 372 ms: 34.41x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (3): unpickle_list, pickle_list, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-CLANG/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.19x