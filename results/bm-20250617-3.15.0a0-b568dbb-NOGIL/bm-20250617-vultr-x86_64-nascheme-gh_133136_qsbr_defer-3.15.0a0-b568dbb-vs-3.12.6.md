# Results vs. 3.12.6

- fork: nascheme
- ref: gh_133136_qsbr_defer
- machine: linux-x86_64
- commit hash: b568dbb
- commit date: 2025-06-17
- overall geometric mean: 1.017x faster
- HPT reliability: 77.28%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 282 ms: 1.07x slower                                                    |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                  |
| html5lib       | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                    |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 504 ms: 1.42x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                   |
| pidigits       | 184 ms                                                 | 211 ms: 1.15x slower                                                    |
| nbody          | 89.3 ms                                                | 121 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                   |
| regex_dna      | 168 ms                                                 | 164 ms: 1.03x faster                                                    |
| regex_v8       | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                   |
| regex_compile  | 142 ms                                                 | 142 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.10x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                   |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                   |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 38.9 ms: 1.12x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                   |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                   |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 526 ms: 2.11x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.85x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 504 ms: 1.42x faster                                                    |
| deepcopy                   | 352 us                                                 | 288 us: 1.22x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                   |
| float                      | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 34.6 us: 1.16x faster                                                   |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.4 us: 1.14x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| generators                 | 32.2 ms                                                | 30.0 ms: 1.08x faster                                                   |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                    |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.03x faster                                                    |
| raytrace                   | 299 ms                                                 | 292 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.01 us: 1.02x faster                                                   |
| chaos                      | 62.8 ms                                                | 62.0 ms: 1.01x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                    |
| regex_compile              | 142 ms                                                 | 142 ms: 1.00x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                  |
| html5lib                   | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.30 ms: 1.02x slower                                                   |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                    |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                    |
| json                       | 5.02 ms                                                | 5.29 ms: 1.05x slower                                                   |
| scimark_fft                | 342 ms                                                 | 363 ms: 1.06x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                   |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                    |
| 2to3                       | 264 ms                                                 | 282 ms: 1.07x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                    |
| nqueens                    | 80.1 ms                                                | 85.8 ms: 1.07x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.10x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 75.4 ms: 1.10x slower                                                   |
| thrift                     | 791 us                                                 | 874 us: 1.10x slower                                                    |
| sympy_expand               | 468 ms                                                 | 517 ms: 1.11x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 85.4 ms: 1.11x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                   |
| django_template            | 34.7 ms                                                | 38.9 ms: 1.12x slower                                                   |
| richards                   | 45.9 ms                                                | 51.6 ms: 1.12x slower                                                   |
| pidigits                   | 184 ms                                                 | 211 ms: 1.15x slower                                                    |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                   |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.69 us: 1.16x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                    |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 871 ms: 1.17x slower                                                    |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                   |
| logging_format             | 7.35 us                                                | 8.70 us: 1.18x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.80 sec: 1.18x slower                                                  |
| fannkuch                   | 372 ms                                                 | 461 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.51 ms: 1.25x slower                                                   |
| telco                      | 6.53 ms                                                | 8.51 ms: 1.30x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.36x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.37x slower                                                   |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                   |
| coverage                   | 71.4 ms                                                | 109 ms: 1.53x slower                                                    |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                   |
| logging_silent             | 109 ns                                                 | 531 ns: 4.88x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 104 ms: 9.66x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (2): pylint, deltablue
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250617-3.15.0a0-b568dbb-NOGIL/bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 77.28% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x