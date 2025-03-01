# Results vs. 3.12.6

- fork: tom-pytel
- ref: fix_issue_128942
- machine: linux-x86_64
- commit hash: 0bcde5c
- commit date: 2025-02-27
- overall geometric mean: 1.058x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 306 ms: 1.16x slower                                                    |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                  |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 340 ms: 1.63x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                    |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                   |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                    |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                  | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                   |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| regex_compile  | 142 ms                                                 | 156 ms: 1.10x slower                                                    |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 251 us: 1.14x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.41 sec: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.4 ms: 1.19x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 369 us: 1.20x slower                                                    |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.6 ms: 1.21x slower                                                   |
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                   |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                   |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.02x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 340 ms: 1.63x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                    |
| deepcopy                   | 352 us                                                 | 313 us: 1.13x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| float                      | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                    |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                    |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                   |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                    |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.85 sec: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                    |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.22 us: 1.05x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                                   |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                  |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.16 us: 1.08x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                    |
| regex_compile              | 142 ms                                                 | 156 ms: 1.10x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.4 us: 1.11x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.82 ms: 1.11x slower                                                   |
| chaos                      | 62.8 ms                                                | 70.0 ms: 1.11x slower                                                   |
| scimark_sor                | 130 ms                                                 | 145 ms: 1.12x slower                                                    |
| thrift                     | 791 us                                                 | 886 us: 1.12x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 835 ms: 1.12x slower                                                    |
| pyflate                    | 448 ms                                                 | 503 ms: 1.12x slower                                                    |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                   |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.73 sec: 1.13x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 251 us: 1.14x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.41 sec: 1.14x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.16x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 88.5 ms: 1.16x slower                                                   |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                                    |
| 2to3                       | 264 ms                                                 | 306 ms: 1.16x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 61.8 ms: 1.16x slower                                                   |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.29 ms: 1.18x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                   |
| sympy_expand               | 468 ms                                                 | 554 ms: 1.19x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 70.4 ms: 1.19x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 369 us: 1.20x slower                                                    |
| nqueens                    | 80.1 ms                                                | 96.4 ms: 1.20x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.44 ms: 1.21x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 60.6 ms: 1.21x slower                                                   |
| richards                   | 45.9 ms                                                | 56.2 ms: 1.22x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                    |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                   |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                    |
| richards_super             | 51.9 ms                                                | 67.4 ms: 1.30x slower                                                   |
| telco                      | 6.53 ms                                                | 8.59 ms: 1.32x slower                                                   |
| fannkuch                   | 372 ms                                                 | 498 ms: 1.34x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                   |
| coverage                   | 71.4 ms                                                | 96.7 ms: 1.35x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 158 ms: 1.38x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 96.4 ms: 1.41x slower                                                   |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                   |
| scimark_fft                | 342 ms                                                 | 500 ms: 1.46x slower                                                    |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 7.78 ms: 1.77x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 95.5 ms: 8.84x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                            |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250227-3.14.0a5+-0bcde5c-NOGIL/bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x