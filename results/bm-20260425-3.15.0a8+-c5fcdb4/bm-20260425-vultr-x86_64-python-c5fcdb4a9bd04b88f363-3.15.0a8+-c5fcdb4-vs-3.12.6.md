# Results vs. 3.12.6

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: linux-x86_64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.46 sec: 1.07x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.5 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 584 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 446 ms: 1.16x faster                                                   |
| async_generators           | 384 ms                                                 | 346 ms: 1.11x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| nbody          | 89.3 ms                                                | 93.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.61 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pickle_dict          | 31.8 us                                                | 30.4 us: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 308 us: 1.00x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 87.1 ms: 1.02x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                  |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                  |
| pickle_list          | 4.77 us                                                | 4.99 us: 1.05x slower                                                  |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.17 us: 1.11x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 6.82 ms: 1.05x faster                                                  |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.0 ms: 1.08x faster                                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 116 ms: 2.74x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                 |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 584 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                   |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.9 us: 1.50x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                  |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                   |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                   |
| spectral_norm              | 110 ms                                                 | 93.6 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.17x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 446 ms: 1.16x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.2 ms: 1.16x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.11 sec: 1.15x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.75 us: 1.15x faster                                                  |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 45.5 ns: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| logging_format             | 7.35 us                                                | 6.45 us: 1.14x faster                                                  |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 346 ms: 1.11x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 69.8 ms: 1.10x faster                                                  |
| logging_silent             | 109 ns                                                 | 99.3 ns: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                  |
| richards                   | 45.9 ms                                                | 42.2 ms: 1.09x faster                                                  |
| scimark_fft                | 342 ms                                                 | 314 ms: 1.09x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.0 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.61 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.2 ms: 1.08x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.6 ms: 1.07x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.46 sec: 1.07x faster                                                 |
| html5lib                   | 63.6 ms                                                | 59.5 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.07x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 64.4 ms: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.27 ms: 1.05x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 6.82 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pickle_dict                | 31.8 us                                                | 30.4 us: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                   |
| thrift                     | 791 us                                                 | 767 us: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                   |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 725 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 161 us: 1.01x faster                                                   |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 308 us: 1.00x slower                                                   |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 472 ms: 1.01x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 87.1 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 383 ms: 1.03x slower                                                   |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                  |
| nbody                      | 89.3 ms                                                | 93.2 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.99 us: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| unpickle                   | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.17 us: 1.11x slower                                                  |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.1 ms: 1.15x slower                                                  |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.36 ms: 1.26x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.41x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.77x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.22x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 273 ms: 25.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): genshi_xml, scimark_sparse_mat_mult
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x