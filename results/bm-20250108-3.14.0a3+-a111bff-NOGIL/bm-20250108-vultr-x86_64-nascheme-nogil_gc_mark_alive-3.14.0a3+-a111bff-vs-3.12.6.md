# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.161x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 342 ms: 1.30x slower                                                    |
| docutils       | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                  |
| html5lib       | 63.6 ms                                                | 89.1 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 734 ms: 1.51x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 762 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 319 ms: 1.40x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 402 ms: 1.39x faster                                                    |
| async_tree_none            | 464 ms                                                 | 353 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 568 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 597 ms: 1.20x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                    |
| float          | 80.8 ms                                                | 106 ms: 1.31x slower                                                    |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| regex_compile  | 142 ms                                                 | 167 ms: 1.17x slower                                                    |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| json_loads           | 26.5 us                                                | 29.0 us: 1.09x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 323 us: 1.47x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 491 us: 1.60x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                   |
| genshi_text     | 22.8 ms                                                | 30.7 ms: 1.34x slower                                                   |
| django_template | 34.7 ms                                                | 48.5 ms: 1.40x slower                                                   |
| mako            | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 734 ms: 1.51x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 762 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 319 ms: 1.40x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 402 ms: 1.39x faster                                                    |
| async_tree_none            | 464 ms                                                 | 353 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 568 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 597 ms: 1.20x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                   |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.10 us: 1.05x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                   |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 40.7 us: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.95 sec: 1.05x slower                                                  |
| pylint                     | 319 ms                                                 | 336 ms: 1.05x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.67 ms: 1.06x slower                                                   |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.0 us: 1.09x slower                                                   |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| scimark_fft                | 342 ms                                                 | 378 ms: 1.11x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.41 us: 1.11x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 89.7 ms: 1.14x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.34 sec: 1.15x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                   |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 89.8 ms: 1.17x slower                                                   |
| regex_compile              | 142 ms                                                 | 167 ms: 1.17x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                   |
| nqueens                    | 80.1 ms                                                | 96.1 ms: 1.20x slower                                                   |
| sympy_str                  | 292 ms                                                 | 351 ms: 1.20x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 24.9 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.36 ms: 1.22x slower                                                   |
| generators                 | 32.2 ms                                                | 39.4 ms: 1.22x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 65.5 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 132 ms: 1.23x slower                                                    |
| sympy_expand               | 468 ms                                                 | 579 ms: 1.24x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                   |
| thrift                     | 791 us                                                 | 988 us: 1.25x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.7 ms: 1.27x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.27x slower                                                    |
| fannkuch                   | 372 ms                                                 | 479 ms: 1.29x slower                                                    |
| 2to3                       | 264 ms                                                 | 342 ms: 1.30x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 969 ms: 1.30x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.43 ms: 1.31x slower                                                   |
| float                      | 80.8 ms                                                | 106 ms: 1.31x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                                  |
| logging_simple             | 6.63 us                                                | 8.81 us: 1.33x slower                                                   |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                                   |
| genshi_text                | 22.8 ms                                                | 30.7 ms: 1.34x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                   |
| coverage                   | 71.4 ms                                                | 97.2 ms: 1.36x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 156 ms: 1.36x slower                                                    |
| comprehensions             | 19.8 us                                                | 27.1 us: 1.37x slower                                                   |
| logging_format             | 7.35 us                                                | 10.1 us: 1.37x slower                                                   |
| django_template            | 34.7 ms                                                | 48.5 ms: 1.40x slower                                                   |
| html5lib                   | 63.6 ms                                                | 89.1 ms: 1.40x slower                                                   |
| pyflate                    | 448 ms                                                 | 627 ms: 1.40x slower                                                    |
| richards                   | 45.9 ms                                                | 66.6 ms: 1.45x slower                                                   |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 323 us: 1.47x slower                                                    |
| richards_super             | 51.9 ms                                                | 77.7 ms: 1.50x slower                                                   |
| chaos                      | 62.8 ms                                                | 94.9 ms: 1.51x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 104 ms: 1.51x slower                                                    |
| hexiom                     | 6.17 ms                                                | 9.36 ms: 1.52x slower                                                   |
| mako                       | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                   |
| scimark_sor                | 130 ms                                                 | 202 ms: 1.56x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.65 ms: 1.59x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 491 us: 1.60x slower                                                    |
| raytrace                   | 299 ms                                                 | 494 ms: 1.65x slower                                                    |
| logging_silent             | 109 ns                                                 | 180 ns: 1.66x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.26 ms: 1.67x slower                                                   |
| go                         | 139 ms                                                 | 236 ms: 1.70x slower                                                    |
| deltablue                  | 3.45 ms                                                | 7.25 ms: 2.11x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.36 ms: 3.57x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 94.2 ms: 8.72x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.24x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250108-3.14.0a3+-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.161x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.35x