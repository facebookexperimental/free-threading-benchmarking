# Results vs. 3.12.6

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: db6d52e
- commit date: 2025-06-03
- overall geometric mean: 1.015x faster
- HPT reliability: 84.54%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                    |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                  |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                    |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                    |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                   |
| pidigits       | 184 ms                                                 | 215 ms: 1.17x slower                                                    |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.65 ms: 1.20x faster                                                   |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                    |
| regex_v8       | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                   |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.04x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 94.6 ms: 1.11x slower                                                   |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                   |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.2 ms: 1.13x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                   |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                   |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                  |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                    |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                    |
| deepcopy                   | 352 us                                                 | 289 us: 1.22x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.65 ms: 1.20x faster                                                   |
| float                      | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 35.0 us: 1.15x faster                                                   |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                  |
| generators                 | 32.2 ms                                                | 29.9 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.04x faster                                                    |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.97 us: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                    |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                   |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                    |
| regex_v8                   | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                    |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.30 ms: 1.02x slower                                                   |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                    |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.56 ms: 1.03x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.04x slower                                                    |
| scimark_fft                | 342 ms                                                 | 360 ms: 1.05x slower                                                    |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                   |
| pyflate                    | 448 ms                                                 | 477 ms: 1.06x slower                                                    |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                    |
| sympy_str                  | 292 ms                                                 | 312 ms: 1.07x slower                                                    |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                    |
| thrift                     | 791 us                                                 | 869 us: 1.10x slower                                                    |
| sympy_expand               | 468 ms                                                 | 518 ms: 1.11x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 94.6 ms: 1.11x slower                                                   |
| richards                   | 45.9 ms                                                | 51.2 ms: 1.11x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 77.3 ms: 1.13x slower                                                   |
| django_template            | 34.7 ms                                                | 39.2 ms: 1.13x slower                                                   |
| richards_super             | 51.9 ms                                                | 58.7 ms: 1.13x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                   |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 188 us: 1.15x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.64 us: 1.15x slower                                                   |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                   |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                    |
| pidigits                   | 184 ms                                                 | 215 ms: 1.17x slower                                                    |
| logging_format             | 7.35 us                                                | 8.68 us: 1.18x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 880 ms: 1.18x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.81 sec: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.26 ms: 1.20x slower                                                   |
| fannkuch                   | 372 ms                                                 | 466 ms: 1.25x slower                                                    |
| telco                      | 6.53 ms                                                | 8.63 ms: 1.32x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                                   |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                   |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                    |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.30x slower                                                   |
| logging_silent             | 109 ns                                                 | 526 ns: 4.83x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.55x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (1): chaos
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 84.54% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x