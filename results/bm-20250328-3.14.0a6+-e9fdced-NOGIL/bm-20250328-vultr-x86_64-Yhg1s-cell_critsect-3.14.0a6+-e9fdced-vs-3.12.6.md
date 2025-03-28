# Results vs. 3.12.6

- fork: Yhg1s
- ref: cell_critsect
- machine: linux-x86_64
- commit hash: e9fdced
- commit date: 2025-03-28
- overall geometric mean: 1.045x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 300 ms: 1.14x slower                                           |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                         |
| html5lib       | 63.6 ms                                                | 70.0 ms: 1.10x slower                                          |
| Geometric mean | (ref)                                                  | 1.10x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                           |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                           |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 525 ms: 1.36x faster                                           |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                          |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                   |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.2 ms: 1.05x faster                                          |
| pidigits       | 184 ms                                                 | 189 ms: 1.02x slower                                           |
| nbody          | 89.3 ms                                                | 138 ms: 1.55x slower                                           |
| Geometric mean | (ref)                                                  | 1.15x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.19x faster                                          |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                           |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.07x slower                                          |
| regex_compile  | 142 ms                                                 | 158 ms: 1.11x slower                                           |
| Geometric mean | (ref)                                                  | 1.01x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                          |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                           |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                          |
| tomli_loads          | 2.11 sec                                               | 2.38 sec: 1.13x slower                                         |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                          |
| unpickle_pure_python | 221 us                                                 | 256 us: 1.16x slower                                           |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                           |
| xml_etree_process    | 59.0 ms                                                | 70.3 ms: 1.19x slower                                          |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.22x slower                                          |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                          |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                          |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.7 ms: 1.21x slower                                          |
| django_template | 34.7 ms                                                | 43.1 ms: 1.24x slower                                          |
| genshi_text     | 22.8 ms                                                | 28.7 ms: 1.26x slower                                          |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                          |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                           |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.90x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                           |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                           |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 525 ms: 1.36x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.19x faster                                          |
| deepcopy                   | 352 us                                                 | 310 us: 1.13x faster                                           |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                          |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                          |
| dulwich_log                | 78.9 ms                                                | 73.1 ms: 1.08x faster                                          |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                           |
| float                      | 80.8 ms                                                | 77.2 ms: 1.05x faster                                          |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                          |
| deepcopy_memo              | 40.3 us                                                | 39.6 us: 1.02x faster                                          |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                          |
| bpe_tokeniser              | 4.74 sec                                               | 4.81 sec: 1.01x slower                                         |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                          |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                         |
| pidigits                   | 184 ms                                                 | 189 ms: 1.02x slower                                           |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                           |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                          |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                           |
| go                         | 139 ms                                                 | 146 ms: 1.05x slower                                           |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                         |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                           |
| scimark_sor                | 130 ms                                                 | 137 ms: 1.06x slower                                           |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                          |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.07x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                          |
| thrift                     | 791 us                                                 | 868 us: 1.10x slower                                           |
| logging_simple             | 6.63 us                                                | 7.27 us: 1.10x slower                                          |
| html5lib                   | 63.6 ms                                                | 70.0 ms: 1.10x slower                                          |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                         |
| regex_compile              | 142 ms                                                 | 158 ms: 1.11x slower                                           |
| chaos                      | 62.8 ms                                                | 69.5 ms: 1.11x slower                                          |
| raytrace                   | 299 ms                                                 | 332 ms: 1.11x slower                                           |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                           |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                          |
| pprint_safe_repr           | 743 ms                                                 | 830 ms: 1.12x slower                                           |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                          |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                           |
| pyflate                    | 448 ms                                                 | 505 ms: 1.13x slower                                           |
| tomli_loads                | 2.11 sec                                               | 2.38 sec: 1.13x slower                                         |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                          |
| deltablue                  | 3.45 ms                                                | 3.91 ms: 1.13x slower                                          |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                         |
| 2to3                       | 264 ms                                                 | 300 ms: 1.14x slower                                           |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                           |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                          |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                          |
| unpickle_pure_python       | 221 us                                                 | 256 us: 1.16x slower                                           |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                           |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                           |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                           |
| xml_etree_process          | 59.0 ms                                                | 70.3 ms: 1.19x slower                                          |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 60.7 ms: 1.21x slower                                          |
| nqueens                    | 80.1 ms                                                | 97.7 ms: 1.22x slower                                          |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.22x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                           |
| hexiom                     | 6.17 ms                                                | 7.59 ms: 1.23x slower                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 84.6 ms: 1.24x slower                                          |
| richards_super             | 51.9 ms                                                | 64.2 ms: 1.24x slower                                          |
| django_template            | 34.7 ms                                                | 43.1 ms: 1.24x slower                                          |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                           |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                           |
| genshi_text                | 22.8 ms                                                | 28.7 ms: 1.26x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.78 ms: 1.32x slower                                          |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                           |
| telco                      | 6.53 ms                                                | 9.03 ms: 1.38x slower                                          |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                          |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                           |
| nbody                      | 89.3 ms                                                | 138 ms: 1.55x slower                                           |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                          |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                          |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                          |
| bench_mp_pool              | 10.8 ms                                                | 96.9 ms: 8.97x slower                                          |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                   |

Benchmark hidden because not significant (3): pylint, async_generators, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250328-3.14.0a6+-e9fdced-NOGIL/bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.37x