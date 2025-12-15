# Results vs. 3.12.6

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.034x slower
- HPT reliability: 84.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 526 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 459 ms: 1.13x faster                                                   |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.75 sec: 1.16x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 123 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pickle_dict          | 31.8 us                                                | 32.1 us: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_list          | 4.77 us                                                | 5.14 us: 1.08x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.30 sec: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| unpickle             | 14.1 us                                                | 16.3 us: 1.16x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.3 ms: 1.19x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.64 us: 1.21x slower                                                  |
| json_loads           | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                  |
| django_template | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.16 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 526 ms: 1.37x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.5 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                                   |
| deepcopy                   | 352 us                                                 | 279 us: 1.26x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 459 ms: 1.13x faster                                                   |
| float                      | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.2 ms: 1.11x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                                   |
| generators                 | 32.2 ms                                                | 30.9 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.98 us: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                   |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                   |
| pickle_dict                | 31.8 us                                                | 32.1 us: 1.01x slower                                                  |
| pyflate                    | 448 ms                                                 | 458 ms: 1.02x slower                                                   |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.87 us: 1.04x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.40 ms: 1.04x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 788 ms: 1.06x slower                                                   |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                   |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| logging_format             | 7.35 us                                                | 7.86 us: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.14 us: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.30 sec: 1.09x slower                                                 |
| json                       | 5.02 ms                                                | 5.48 ms: 1.09x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 57.0 ns: 1.10x slower                                                  |
| thrift                     | 791 us                                                 | 882 us: 1.11x slower                                                   |
| nqueens                    | 80.1 ms                                                | 89.3 ms: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                  |
| richards                   | 45.9 ms                                                | 51.7 ms: 1.12x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.90 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.6 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.5 ms: 1.15x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                   |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.75 sec: 1.16x slower                                                 |
| unpickle                   | 14.1 us                                                | 16.3 us: 1.16x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                  |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.18x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                                   |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.3 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.28 ms: 1.20x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.64 us: 1.21x slower                                                  |
| json_loads                 | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.35x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                  |
| nbody                      | 89.3 ms                                                | 123 ms: 1.37x slower                                                   |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 176 ms: 27.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (3): scimark_fft, chaos, regex_compile
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-NOGIL/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x slower

# HPT report

- Reliability score: 84.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x