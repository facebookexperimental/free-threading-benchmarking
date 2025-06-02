# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.591x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| html5lib       | 63.6 ms                                                | 62.2 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 625 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 502 ms: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 65.0 ms: 1.24x faster                                                 |
| nbody          | 89.3 ms                                                | 82.6 ms: 1.08x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.52 ms: 1.26x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.78 sec: 1.18x faster                                                |
| unpickle_pure_python | 221 us                                                 | 191 us: 1.16x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 53.4 ms: 1.10x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                 |
| unpickle             | 14.1 us                                                | 13.9 us: 1.01x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                  |
| pickle_dict          | 31.8 us                                                | 32.8 us: 1.03x slower                                                 |
| unpickle_list        | 4.67 us                                                | 4.87 us: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.09 us: 1.07x slower                                                 |
| pickle               | 10.9 us                                                | 12.5 us: 1.14x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                 |
| mako            | 11.0 ms                                                | 11.1 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pprint_pformat             | 1.52 sec                                               | 1.38 us: 1104094.21x faster                                           |
| pprint_safe_repr           | 743 ms                                                 | 797 ns: 932783.73x faster                                             |
| mdp                        | 2.42 sec                                               | 1.17 sec: 2.07x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 625 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                  |
| richards                   | 45.9 ms                                                | 32.2 ms: 1.43x faster                                                 |
| richards_super             | 51.9 ms                                                | 36.7 ms: 1.41x faster                                                 |
| deepcopy                   | 352 us                                                 | 249 us: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.1 us: 1.38x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.52 ms: 1.26x faster                                                 |
| float                      | 80.8 ms                                                | 65.0 ms: 1.24x faster                                                 |
| spectral_norm              | 110 ms                                                 | 89.6 ms: 1.23x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.7 us: 1.19x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.91 ms: 1.18x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.00 sec: 1.18x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.78 sec: 1.18x faster                                                |
| scimark_fft                | 342 ms                                                 | 289 ms: 1.18x faster                                                  |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.17x faster                                                 |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 191 us: 1.16x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.66 us: 1.15x faster                                                 |
| pyflate                    | 448 ms                                                 | 393 ms: 1.14x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 60.5 ms: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 53.4 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.8 ms: 1.10x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| nbody                      | 89.3 ms                                                | 82.6 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.08x faster                                                 |
| thrift                     | 791 us                                                 | 746 us: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.5 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 502 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| nqueens                    | 80.1 ms                                                | 78.3 ms: 1.02x faster                                                 |
| html5lib                   | 63.6 ms                                                | 62.2 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.02x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.9 us: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                                  |
| sympy_expand               | 468 ms                                                 | 464 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                |
| mako                       | 11.0 ms                                                | 11.1 ms: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.69 us: 1.01x slower                                                 |
| logging_format             | 7.35 us                                                | 7.43 us: 1.01x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.26 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.8 us: 1.03x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.87 us: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.09 us: 1.07x slower                                                 |
| telco                      | 6.53 ms                                                | 7.13 ms: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| pickle                     | 10.9 us                                                | 12.5 us: 1.14x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.9 ms: 1.15x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 61.7 ns: 1.19x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.54 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.90 ms: 1.74x slower                                                 |
| logging_silent             | 109 ns                                                 | 465 ns: 4.27x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.3 ms: 9.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                          |

Benchmark hidden because not significant (4): regex_dna, asyncio_websockets, scimark_sparse_mat_mult, json
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, regex_compile, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.591x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.16x