# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: fix_issue_128942
- machine: linux-x86_64
- commit hash: 0bcde5c
- commit date: 2025-02-27
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 306 ms: 1.18x slower                                                    |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                  |
| html5lib       | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 241 ms: 1.38x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 512 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                    |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 216 ms: 1.00x faster                                                    |
| nbody          | 85.3 ms                                                                | 133 ms: 1.56x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                   |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| regex_compile  | 131 ms                                                                 | 156 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                    |
| json_loads           | 27.3 us                                                                | 29.4 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 70.4 ms: 1.19x slower                                                   |
| tomli_loads          | 2.01 sec                                                               | 2.41 sec: 1.20x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 251 us: 1.21x slower                                                    |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 369 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.68 ms: 1.30x slower                                                   |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.6 ms: 1.23x slower                                                   |
| django_template | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                   |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                   |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 241 ms: 1.38x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 512 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                    |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                    |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.04x faster                                                   |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                    |
| pidigits                   | 216 ms                                                                 | 216 ms: 1.00x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                   |
| deepcopy_memo              | 38.1 us                                                                | 38.4 us: 1.01x slower                                                   |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.02x slower                                                   |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.22 us: 1.03x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                  |
| json_loads                 | 27.3 us                                                                | 29.4 us: 1.07x slower                                                   |
| scimark_sor                | 134 ms                                                                 | 145 ms: 1.09x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.85 sec: 1.09x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.59 ms: 1.11x slower                                                   |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 82.7 ms: 1.11x slower                                                   |
| pyflate                    | 449 ms                                                                 | 503 ms: 1.12x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                                   |
| thrift                     | 772 us                                                                 | 886 us: 1.15x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 113 ns: 1.16x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 122 ms: 1.16x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 835 ms: 1.16x slower                                                    |
| logging_simple             | 6.14 us                                                                | 7.16 us: 1.17x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.73 sec: 1.17x slower                                                  |
| coverage                   | 82.5 ms                                                                | 96.7 ms: 1.17x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.8 ms: 1.17x slower                                                   |
| 2to3                       | 259 ms                                                                 | 306 ms: 1.18x slower                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 70.4 ms: 1.19x slower                                                   |
| regex_compile              | 131 ms                                                                 | 156 ms: 1.19x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.41 sec: 1.20x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.30 us: 1.20x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 251 us: 1.21x slower                                                    |
| comprehensions             | 16.6 us                                                                | 20.1 us: 1.21x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 554 ms: 1.22x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 337 ms: 1.23x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 60.6 ms: 1.23x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.82 ms: 1.23x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 96.4 ms: 1.24x slower                                                   |
| django_template            | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.93 ms: 1.24x slower                                                   |
| chaos                      | 56.3 ms                                                                | 70.0 ms: 1.24x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.44 ms: 1.25x slower                                                   |
| richards                   | 44.4 ms                                                                | 56.2 ms: 1.26x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 369 us: 1.26x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.28x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.29x slower                                                   |
| raytrace                   | 250 ms                                                                 | 322 ms: 1.29x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 88.5 ms: 1.30x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.68 ms: 1.30x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 498 ms: 1.32x slower                                                    |
| richards_super             | 50.4 ms                                                                | 67.4 ms: 1.34x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 158 ms: 1.41x slower                                                    |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 500 ms: 1.43x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 96.4 ms: 1.47x slower                                                   |
| nbody                      | 85.3 ms                                                                | 133 ms: 1.56x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 7.78 ms: 1.64x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.57x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 95.5 ms: 8.68x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                            |

Benchmark hidden because not significant (3): pylint, float, go
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250227-3.14.0a5+-0bcde5c-NOGIL/bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.34x