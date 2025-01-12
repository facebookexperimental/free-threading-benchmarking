# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.151x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 339 ms: 1.29x slower                                                    |
| docutils       | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                  |
| html5lib       | 63.6 ms                                                | 88.3 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                  | 1.26x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 727 ms: 1.53x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 757 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 315 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 427 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 574 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 447 ms: 1.16x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                    |
| float          | 80.8 ms                                                | 105 ms: 1.30x slower                                                    |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                    |
| Geometric mean | (ref)                                                  | 1.22x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                   |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                    |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                   |
| regex_compile  | 142 ms                                                 | 165 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.8 ms: 1.33x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 320 us: 1.45x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 489 us: 1.59x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.0 ms: 1.24x slower                                                   |
| genshi_text     | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                   |
| django_template | 34.7 ms                                                | 49.5 ms: 1.43x slower                                                   |
| mako            | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 727 ms: 1.53x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 757 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 315 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 427 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 574 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                   |
| deepcopy                   | 352 us                                                 | 323 us: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.10 us: 1.05x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.35 ms: 1.03x faster                                                   |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                    |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.01x slower                                                    |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.90 sec: 1.03x slower                                                  |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                   |
| pylint                     | 319 ms                                                 | 335 ms: 1.05x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.37 us: 1.09x slower                                                   |
| scimark_fft                | 342 ms                                                 | 376 ms: 1.10x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.67 sec: 1.10x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 89.9 ms: 1.14x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.15x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 192 ms: 1.16x slower                                                    |
| regex_compile              | 142 ms                                                 | 165 ms: 1.16x slower                                                    |
| async_generators           | 384 ms                                                 | 447 ms: 1.16x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 89.2 ms: 1.16x slower                                                   |
| nqueens                    | 80.1 ms                                                | 95.6 ms: 1.19x slower                                                   |
| sympy_str                  | 292 ms                                                 | 350 ms: 1.20x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 24.8 ms: 1.21x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 65.0 ms: 1.22x slower                                                   |
| generators                 | 32.2 ms                                                | 39.4 ms: 1.22x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 131 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                    |
| sympy_expand               | 468 ms                                                 | 577 ms: 1.23x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 62.0 ms: 1.24x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                   |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                    |
| thrift                     | 791 us                                                 | 999 us: 1.26x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 939 ms: 1.26x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 181 ms: 1.27x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.6 ms: 1.27x slower                                                   |
| fannkuch                   | 372 ms                                                 | 474 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.59 ms: 1.27x slower                                                   |
| 2to3                       | 264 ms                                                 | 339 ms: 1.29x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.95 sec: 1.29x slower                                                  |
| float                      | 80.8 ms                                                | 105 ms: 1.30x slower                                                    |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.45 ms: 1.33x slower                                                   |
| genshi_text                | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.8 ms: 1.33x slower                                                   |
| logging_simple             | 6.63 us                                                | 8.96 us: 1.35x slower                                                   |
| comprehensions             | 19.8 us                                                | 26.9 us: 1.36x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.36x slower                                                    |
| logging_format             | 7.35 us                                                | 10.0 us: 1.36x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                   |
| coverage                   | 71.4 ms                                                | 97.4 ms: 1.36x slower                                                   |
| html5lib                   | 63.6 ms                                                | 88.3 ms: 1.39x slower                                                   |
| pyflate                    | 448 ms                                                 | 625 ms: 1.40x slower                                                    |
| richards                   | 45.9 ms                                                | 64.7 ms: 1.41x slower                                                   |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                    |
| richards_super             | 51.9 ms                                                | 73.8 ms: 1.42x slower                                                   |
| django_template            | 34.7 ms                                                | 49.5 ms: 1.43x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 320 us: 1.45x slower                                                    |
| chaos                      | 62.8 ms                                                | 91.7 ms: 1.46x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 101 ms: 1.47x slower                                                    |
| hexiom                     | 6.17 ms                                                | 9.11 ms: 1.48x slower                                                   |
| scimark_sor                | 130 ms                                                 | 199 ms: 1.53x slower                                                    |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.62 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 489 us: 1.59x slower                                                    |
| raytrace                   | 299 ms                                                 | 483 ms: 1.62x slower                                                    |
| go                         | 139 ms                                                 | 226 ms: 1.62x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.25 ms: 1.66x slower                                                   |
| logging_silent             | 109 ns                                                 | 184 ns: 1.68x slower                                                    |
| deltablue                  | 3.45 ms                                                | 7.06 ms: 2.05x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 93.8 ms: 8.69x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.22x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250111-3.14.0a3+-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.151x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.35x